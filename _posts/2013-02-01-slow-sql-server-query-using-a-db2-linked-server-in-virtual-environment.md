---
title: Slow SQL Server query using a DB2 linked server in virtual environment
date: 2013-02-01 10:04:40.000000000 -08:00
category: blog
tag:
- work
- performance
- SQL Server
---
<p>We ran into an issue at work where a SQL Server query was slow when the VM in which the SQL Server was running in had more than 1 vCore. I had posted the question on dba.se and was able to piece together an answer so I wanted to keep a record of that here as well.</p>
<p><strong>Environment</strong></p>
<ul>
<li>Virtual Windows 2003 R2 server (fresh deployments on XenServer 6.1 & ESXi 5)</li>
<li>SQL Server 2005 SP3</li>
<li>Linked Server created using IBM DB2 for iBMASQL OLE DB Provider</li>
</ul>
<p><a href="http://stanleylee.hk/wp-content/uploads/2013/02/linksrv.jpg"><img src="{{ site.baseurl }}/assets/images/linksrv.jpg" alt="linksrv" width="521" height="538" class="alignnone size-full wp-image-222" /></a></p>
<p><strong>Query</strong></p>
<ul>
<li>The query itself is a select statement with a where clause which selects transactions this month.<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/02/query.jpg"><img src="{{ site.baseurl }}/assets/images/query.jpg" alt="query" width="505" height="869" class="alignnone size-full wp-image-223" /></a></li>
</ul>
<p><strong>Issue</strong></p>
<ul>
<li>Virtual machine is set to 4 vCores, it takes roughly 35 seconds to complete</li>
<li>Virtual machine is set to 2 vCores, it takes roughly 20 seconds to complete</li>
<li>Virtual machine is set to 1 vCores, it takes roughly 5 seconds to complete</li>
</ul>
<p><strong>Solution</strong></p>
<p>The issue is in part due to the CPU affinity setting in SQL.</p>
<p>We deployed this VM with SQL from an image which causes a known issue. Removing the automatic affinity option and setting the affinity mask option to use all the CPUs available resolved the issue.</p>
```sp_configure 'show advanced options', 1;
RECONFIGURE;
GO
sp_configure 'affinity mask', 15;
RECONFIGURE;
GO
sp_configure 'show advanced options', 0;
RECONFIGURE;
GO```
<p><a href="http://stanleylee.hk/wp-content/uploads/2013/02/affinity.jpg"><img src="{{ site.baseurl }}/assets/images/affinity.jpg" alt="affinity" width="487" height="302" class="alignnone size-full wp-image-225" /></a></p>
<p>We have updated our image to include this option.</p>
<p><strong>Notes</strong></p>
<p>Please note, this option is deprecated in SQL Server 2012 and is not recommended for use. Additionally, it is related to processor thread handling in Windows 2000 and Windows 2003 operating systems.</p>
<p><a href="http://dba.stackexchange.com/questions/33861/slow-sql-server-query-using-a-db2-linked-server-in-virtual-environment" title="dba.se question" target="_blank">Original dba.se question</a></p>
