---
title: 'Exam 70-462: Administering Microsoft SQL Server 2012 Databases'
date: 2013-02-01 10:48:36.000000000 -08:00
category: blog
tag:
- study
- 70-462
- Microsoft
---
<p>After reading Katie & Emil's post regarding 70-461 and upon my completion of the exam, I decided that I will do something similar during my studies for the next exam - the 70-462. I know they have a page for 70-462 as well but I thought it would be a good experience to write something up myself to make sure I understand the material.</p>
<p>This is going to be an ongoing project and I will list out the skills measured by Microsoft on this page first. As I update and create separate posts regarding each particular skill, I will link them here.</p>
<p><strong>Exam 70-462: Administering Microsoft SQL Server 2012 Databases</strong><br />
<strong><em>Install and Configure (19%)</em></strong></p>
<ul>
<li><strong>Plan installation.</strong></li>
<ul>
<li><a href="http://stanleylee.hk/2013/02/08/70-462-plan-installation-evaluate-installation-requirements/" title="70-462 – Plan installation – evaluate installation requirements">evaluate installation requirements</a></li>
<li><a href="http://stanleylee.hk/2013/02/08/70-462-plan-installation-design-the-installation-of-sql-server-and-its-components/" title="70-462 – Plan installation – design the installation of SQL Server and its components">design the installation of SQL Server and its components (drives, service accounts etc.)</a></li>
<li>plan scale up vs. scale out basics</li>
<li>plan for capacity, including if/when to shrink, grow, autogrow, and monitor growth</li>
<li>manage the technologies that influence SQL architecture (e.g., service broker, full text, scale out, etc.)</li>
<li>design the storage for new databases (drives, filegroups, partitioning)</li>
<li>design database infrastructure</li>
<li>configure a SQL Server standby database for reporting purposes</li>
<li>Windows-level security and service level security</li>
<li>Core mode installation</li>
<li>benchmark a server before using it in a production environment (SQLIO, Tests on SQL Instance)</li>
<li>choose the right hardware</li>
</ul>
<li><strong>Install SQL Server and related services.</strong></li>
<ul>
<li>test connectivity</li>
<li>enable and disable features</li>
<li>install SQL Server database engine and SSIS (not SSRS and SSAS)</li>
<li>configure an OS disk</li>
</ul>
<li><strong>Implement a migration strategy.</strong></li>
<ul>
<li>restore vs detach/attach</li>
<li>migrate security</li>
<li>migrate from a previous version</li>
<li>migrate to new hardware</li>
<li>migrate systems and data from other sources</li>
</ul>
<li><strong>Configure additional SQL Server components.</strong></li>
<ul>
<li>setup and configure all SQL Server components (Engine, AS, RS and SharePoint integration) in a complex and highly secure environment</li>
<li>configure full-text indexing</li>
<li>SSIS security</li>
<li>filestream</li>
<li>filetable</li>
</ul>
<li><strong>Manage SQL Server Agent.</strong></li>
<ul>
<li>create, maintain, and monitor jobs</li>
<li>administer jobs and alerts</li>
<li>automate (setup, maintenance, monitoring) across multiple databases and multiple instances</li>
<li>send to "Manage SQL Server Agent jobs"</li>
</ul>
</ul>
<p><strong><em>Maintain Instances and Databases (17%)</em></strong></p>
<ul>
<li><strong>Manage and configure databases.</strong></li>
<ul>
<li>design multiple file groups</li>
<li>database configuration and standardization: autoclose, autoshrink, recovery models</li>
<li>manage file space, including adding new filegroups and moving objects from one filegroup to another</li>
<li>implement and configure contained databases</li>
<li>data compression</li>
<li>configure TDE</li>
<li>partitioning</li>
<li>manage log file growth</li>
<li>DBCC</li>
</ul>
<li><strong>Configure SQL Server instances.</strong></li>
<ul>
<li>configure and standardize a database: autoclose, autoshrink, recovery models</li>
<li>install default and named instances</li>
<li>configure SQL to use only certain CPUs (affinity masks, etc.)</li>
<li>configure server level settings</li>
<li>configure many databases/instance, many instances/server, virtualization</li>
<li>configure clustered instances including MSDTC</li>
<li>memory allocation</li>
<li>database mail</li>
<li>configure SQL Server engine: memory, filffactor, sp_configure, default options</li>
</ul>
<li><strong>Implement a SQL Server clustered instance.</strong></li>
<ul>
<li>install a cluster</li>
<li>manage multiple instances on a cluster</li>
<li>set up subnet clustering</li>
<li>recover from a failed cluster node</li>
</ul>
<li><strong>Manage SQL Server instances. </strong></li>
<ul>
<li>install an instance</li>
<li>manage interaction of instances</li>
<li>SQL patch management</li>
<li>install additional instances</li>
<li>manage resource utilization by using Resource Governor</li>
<li>cycle error logs</li>
</ul>
</ul>
<p><strong><em>Optimize and Troubleshoot (14%)</em></strong></p>
<ul>
<li><strong>Identify and resolve concurrency problems.</strong></li>
<ul>
<li>examine deadlocking issues using the SQL server logs using trace flags</li>
<li>design reporting database infrastructure (replicated databases)</li>
<li>monitor via DMV or other MS product</li>
<li>diagnose blocking, live locking and deadlocking</li>
<li>diagnose waits</li>
<li>performance detection with built in DMVs</li>
<li>know what affects performance</li>
<li>locate and if necessary kill processes that are blocking or claiming all resources</li>
</ul>
<li><strong>Collect and analyze troubleshooting data.</strong></li>
<ul>
<li>monitor using Profiler, collect performance data by using System Monitor, Collect trace data by using SQL Server Profiler, identify transactional replication problems</li>
<li>identify and troubleshoot data access problems</li>
<li>gather performance metrics</li>
<li>identify potential problems before they cause service interruptions</li>
<li>identify performance problems, use Xevents and dmvs</li>
<li>create alerts on critical server condition</li>
<li>monitor data and server access by creating audit and other controls</li>
<li>identify IO vs. memory vs. CPU bottlenecks</li>
<li>use the Data Collector tool</li>
</ul>
<li><strong>Audit SQL Server instances.</strong></li>
<ul>
<li>implement a security strategy for auditing and controlling the instance</li>
<li>configure an audit</li>
<li>configure server audits</li>
<li>track who modified an object</li>
<li>monitor elevated privileges as well as unsolicited attempts to connect</li>
<li>policy-based management</li>
</ul>
</ul>
<p><strong><em>Manage Data (19%)</em></strong></p>
<ul>
<li><strong>Configure and maintain a back up strategy.</strong></li>
<ul>
<li>manage different backup models, including point in time recovery</li>
<li>protect customer data even if backup media is lost</li>
<li>perform backup/restore based on proper strategies including backup redundancy</li>
<li>recover from a corrupted drive</li>
<li>manage a multi-TB database</li>
<li>implement and test a database implementation and a backup strategy (multiple files for user database and tempdb, spreading database files, backup/restore)</li>
<li>backup a SQL Server environment</li>
<li>back up system databases</li>
</ul>
<li><strong>Restore databases.</strong></li>
<ul>
<li>restore a database secured with TDE</li>
<li>recover data from a damaged DB (several errors in DBCC checkdb)</li>
<li>restore to a point in time</li>
<li>file group restore</li>
<li>page level restore</li>
</ul>
<li><strong>Implement and maintain indexes.</strong></li>
<ul>
<li>inspect physical characteristics of indexes and perform index maintenance</li>
<li>identify fragmented indexes</li>
<li>identify unused indexes</li>
<li>implement indexes</li>
<li>defrag/rebuild indexes</li>
<li>set up a maintenance strategy for indexes and statistics</li>
<li>optimize indexes (full, filter index)</li>
<li>statistics (full, filter) force or fix queue</li>
<li>when to rebuild vs. reorg and index</li>
<li>full text indexes</li>
<p> column store indexes
	</ul>
<li><strong>Import and export data.</strong></li>
<ul>
<li>transfer data</li>
<li>bulk copy</li>
<li>bulk insert</li>
</ul>
</ul>
<p><strong><em>Implement Security (18%)</em></strong></p>
<ul>
<li><strong>Manage logins and server roles.</strong></li>
<ul>
<li>configure server security</li>
<li>secure the SQL Server using Windows Account / SQL Server accounts, server roles</li>
<li>create log in accounts</li>
<li>manage access to the server, SQL Server instance, and databases</li>
<li>create and maintain user-defined server roles</li>
<li>manage certificate logins</li>
</ul>
<li><strong>Manage database permissions.</strong></li>
<ul>
<li>configure database security</li>
<li>database level, permissions</li>
<li>protect objects from being modified</li>
</ul>
<li><strong>Manage users and database roles. </strong></li>
<ul>
<li>create access to server / database with least privilege</li>
<li>manage security roles for users and administrators</li>
<li>create database user accounts</li>
<li>contained logins</li>
</ul>
<li><strong>Troubleshoot security.</strong></li>
<ul>
<li>manage certificates and keys</li>
<li>endpoints</li>
</ul>
</ul>
<p><strong><em>Implement High Availability (12%)</em></strong></p>
<ul>
<li><strong>Implement AlwaysOn.</strong></li>
<ul>
<li>implement a mirroring solution using AlwaysOn</li>
<li>failover</li>
</ul>
<li><strong>Implement database mirroring.</strong></li>
<ul>
<li>set up mirroring</li>
<li>monitor the performance of database mirroring</li>
</ul>
<li><strong>Implement replication.</strong></li>
<ul>
<li>troubleshoot replication problems</li>
<li>identify appropriate replication strategy</li>
</ul>
</ul>
<p><strong>Reference to Katie & Emil's site:</strong><br />
<a href="http://www.katieandemil.com/exam-70-461-querying-microsoft-sql-server-2012-pdf-vce-ebook-free" title="Katie & Emil - 70-461" target="_blank">Katie & Emil - 70-461</a><br />
<a href="http://www.katieandemil.com/Katie-and-Emil-Tutorial-to-70-462-Administering-Microsoft-SQL-Server-2012-Databases" title="Katie & Emil - 70-462" target="_blank">Katie & Emil - 70-462</a></p>
