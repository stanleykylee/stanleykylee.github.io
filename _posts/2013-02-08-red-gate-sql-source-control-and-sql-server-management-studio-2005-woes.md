---
title: Red Gate SQL Source Control and SQL Server Management Studio 2005 Woes
date: 2013-02-08 11:47:45.000000000 -08:00
category: blog
tag:
- work
- redgate
- sql source control
---
<p>Continuing with supporting Red Gate SQL Source Control, we ran into another issue with the most current release of the software - SQL Source Control 3.1.0.5208. When loading SQL Server Management Studio 2005, we got the following message:</p>
<blockquote><p>Failure to load Add-on</p></blockquote>
<p>This issue didn't happen for our developers who were using SQL Server Management Studio 2008 and 2012 after we resolved our <a href="http://stanleylee.hk/2013/02/05/red-gate-sql-source-control-and-tfs/">proxy issue</a>.</p>
<p>After trying several things, we came to the conclusion that the latest version just did not work and had to revert to using an older version of SQL Source Control, 3.1.0.4829.</p>
<p>This version seemed to work with no issue thus far.</p>
<p>Good luck!</p>
