---
title: Moving scheduled jobs from old to new Microsoft SQL Server
date: 2013-01-16 09:30:29.000000000 -08:00
category: blog
tag:
- work
- scheduler
- SQL Server
---
<p>Somewhat related to my previous post, I was now tasked with moving scheduled jobs from the old Microsoft SQL Server to a new Microsoft SQL Server. To do this, we generated a script within MS SQL Server Management Studio. I came up with a few issues while trying to run the scripts on the new server.</p>
<p><code><br />
Msg 14234, Level 16, State 1, Procedure sp_verify_job, Line 243<br />
The specified '@notify_email_operator_name' is invalid (valid values are returned by sp_help_operator).<br />
</code></p>
<p>With this issue, the operators had not be defined in the new server. A simple fix is to generate a script for each of the Operators from the old server.</p>
<p><code><br />
Msg 8145, Level 16, State 1, Procedure sp_add_jobschedule, Line 0<br />
@schedule_uid is not a parameter for procedure sp_add_jobschedule.<br />
</code></p>
<p>With this issue, it has to do with how the schedule id is kept in the msdb database. </p>
<p><code><br />
select * from sysjobschedules<br />
</code></p>
<p>Running the above will show whether the new SQL server is using schedule_id (an integer) or schedule_uid (an uniqueidentifier). Update the script to reflect the correct schedule id datatype.</p>
<p><code><br />
select newid()<br />
</code></p>
<p>Running the above will generate a new uniqueidentifier if required.</p>
