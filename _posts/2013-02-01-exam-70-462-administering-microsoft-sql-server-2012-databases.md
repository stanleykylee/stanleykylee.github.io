---
title: 'Exam 70-462: Administering Microsoft SQL Server 2012 Databases'
date: 2013-02-01 10:48:36.000000000 -08:00
category: blog
tag:
- study
- 70-462
- Microsoft
---
After reading Katie & Emil's post regarding 70-461 and upon my completion of the exam, I decided that I will do something similar during my studies for the next exam - the 70-462\. I know they have a page for 70-462 as well but I thought it would be a good experience to write something up myself to make sure I understand the material.

This is going to be an ongoing project and I will list out the skills measured by Microsoft on this page first. As I update and create separate posts regarding each particular skill, I will link them here.

**Exam 70-462: Administering Microsoft SQL Server 2012 Databases**  
**_Install and Configure (19%)_**

**Plan installation.**

*   [evaluate installation requirements](http://iamstanlee.com/2013/02/08/70-462-plan-installation-evaluate-installation-requirements/ "70-462 – Plan installation – evaluate installation requirements")
*   [design the installation of SQL Server and its components (drives, service accounts etc.)](http://iamstanlee.com/2013/02/08/70-462-plan-installation-design-the-installation-of-sql-server-and-its-components/ "70-462 – Plan installation – design the installation of SQL Server and its components")
*   plan scale up vs. scale out basics
*   plan for capacity, including if/when to shrink, grow, autogrow, and monitor growth
*   manage the technologies that influence SQL architecture (e.g., service broker, full text, scale out, etc.)
*   design the storage for new databases (drives, filegroups, partitioning)
*   design database infrastructure
*   configure a SQL Server standby database for reporting purposes
*   Windows-level security and service level security
*   Core mode installation
*   benchmark a server before using it in a production environment (SQLIO, Tests on SQL Instance)
*   choose the right hardware

**Install SQL Server and related services.**

*   test connectivity
*   enable and disable features
*   install SQL Server database engine and SSIS (not SSRS and SSAS)
*   configure an OS disk

**Implement a migration strategy.**

*   restore vs detach/attach
*   migrate security
*   migrate from a previous version
*   migrate to new hardware
*   migrate systems and data from other sources

**Configure additional SQL Server components.**

*   setup and configure all SQL Server components (Engine, AS, RS and SharePoint integration) in a complex and highly secure environment
*   configure full-text indexing
*   SSIS security
*   filestream
*   filetable

**Manage SQL Server Agent.**

*   create, maintain, and monitor jobs
*   administer jobs and alerts
*   automate (setup, maintenance, monitoring) across multiple databases and multiple instances
*   send to "Manage SQL Server Agent jobs"

**_Maintain Instances and Databases (17%)_**

**Manage and configure databases.**

*   design multiple file groups
*   database configuration and standardization: autoclose, autoshrink, recovery models
*   manage file space, including adding new filegroups and moving objects from one filegroup to another
*   implement and configure contained databases
*   data compression
*   configure TDE
*   partitioning
*   manage log file growth
*   DBCC

**Configure SQL Server instances.**

*   configure and standardize a database: autoclose, autoshrink, recovery models
*   install default and named instances
*   configure SQL to use only certain CPUs (affinity masks, etc.)
*   configure server level settings
*   configure many databases/instance, many instances/server, virtualization
*   configure clustered instances including MSDTC
*   memory allocation
*   database mail
*   configure SQL Server engine: memory, filffactor, sp_configure, default options

**Implement a SQL Server clustered instance.**

*   install a cluster
*   manage multiple instances on a cluster
*   set up subnet clustering
*   recover from a failed cluster node

**Manage SQL Server instances.**

*   install an instance
*   manage interaction of instances
*   SQL patch management
*   install additional instances
*   manage resource utilization by using Resource Governor
*   cycle error logs

**_Optimize and Troubleshoot (14%)_**

**Identify and resolve concurrency problems.**

*   examine deadlocking issues using the SQL server logs using trace flags
*   design reporting database infrastructure (replicated databases)
*   monitor via DMV or other MS product
*   diagnose blocking, live locking and deadlocking
*   diagnose waits
*   performance detection with built in DMVs
*   know what affects performance
*   locate and if necessary kill processes that are blocking or claiming all resources

**Collect and analyze troubleshooting data.**

*   monitor using Profiler, collect performance data by using System Monitor, Collect trace data by using SQL Server Profiler, identify transactional replication problems
*   identify and troubleshoot data access problems
*   gather performance metrics
*   identify potential problems before they cause service interruptions
*   identify performance problems, use Xevents and dmvs
*   create alerts on critical server condition
*   monitor data and server access by creating audit and other controls
*   identify IO vs. memory vs. CPU bottlenecks
*   use the Data Collector tool

**Audit SQL Server instances.**

*   implement a security strategy for auditing and controlling the instance
*   configure an audit
*   configure server audits
*   track who modified an object
*   monitor elevated privileges as well as unsolicited attempts to connect
*   policy-based management

**_Manage Data (19%)_**

**Configure and maintain a back up strategy.**

*   manage different backup models, including point in time recovery
*   protect customer data even if backup media is lost
*   perform backup/restore based on proper strategies including backup redundancy
*   recover from a corrupted drive
*   manage a multi-TB database
*   implement and test a database implementation and a backup strategy (multiple files for user database and tempdb, spreading database files, backup/restore)
*   backup a SQL Server environment
*   back up system databases

**Restore databases.**

*   restore a database secured with TDE
*   recover data from a damaged DB (several errors in DBCC checkdb)
*   restore to a point in time
*   file group restore
*   page level restore

**Implement and maintain indexes.**

*   inspect physical characteristics of indexes and perform index maintenance
*   identify fragmented indexes
*   identify unused indexes
*   implement indexes
*   defrag/rebuild indexes
*   set up a maintenance strategy for indexes and statistics
*   optimize indexes (full, filter index)
*   statistics (full, filter) force or fix queue
*   when to rebuild vs. reorg and index
*   full text indexes
*   column store indexes

**Import and export data.**

*   transfer data
*   bulk copy
*   bulk insert

**_Implement Security (18%)_**

**Manage logins and server roles.**

*   configure server security
*   secure the SQL Server using Windows Account / SQL Server accounts, server roles
*   create log in accounts
*   manage access to the server, SQL Server instance, and databases
*   create and maintain user-defined server roles
*   manage certificate logins

**Manage database permissions.**

*   configure database security
*   database level, permissions
*   protect objects from being modified

**Manage users and database roles.**

*   create access to server / database with least privilege
*   manage security roles for users and administrators
*   create database user accounts
*   contained logins

**Troubleshoot security.**

*   manage certificates and keys
*   endpoints

**_Implement High Availability (12%)_**

**Implement AlwaysOn.**

*   implement a mirroring solution using AlwaysOn
*   failover

**Implement database mirroring.**

*   set up mirroring
*   monitor the performance of database mirroring

**Implement replication.**

*   troubleshoot replication problems
*   identify appropriate replication strategy

**Reference to Katie & Emil's site:**  
[Katie & Emil - 70-461](http://www.katieandemil.com/exam-70-461-querying-microsoft-sql-server-2012-pdf-vce-ebook-free "Katie & Emil - 70-461")  
[Katie & Emil - 70-462](http://www.katieandemil.com/Katie-and-Emil-Tutorial-to-70-462-Administering-Microsoft-SQL-Server-2012-Databases "Katie & Emil - 70-462")