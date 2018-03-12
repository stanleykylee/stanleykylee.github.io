---
title: CDONTS on Windows Server 2008 R2
date: 2011-02-08 10:49:28.000000000 -08:00
category: blog
tag:
- web
- work
- CDONTS
- windows 2008 r2
---
<p>As old as it may be, we still use a sendmail API from way back to NT4! Having said that, there was a slight blip when we migrated to a new Server 2008 R2 server, the dll file was missing! I had to copy the file from the old server and move it to the new server.</p>
<ol>
<li>Copy CDONTS.dll from another server to C:\Windows\SysWOW64 and C:\Windows\System32</li>
<li>Run regsvr32 c:\windows\SysWOW64\cdonts.dll</li>
<li>Run regsvr32 c:\windows\System32\cdonts.dll</li>
<li>Grant the appropriate permissions on C:\inetpub\mailroot\pickup (I granted USERS group Modify permissions).  You could get permission denied if the folder security isn't adjusted.</li>
</ol>
<p>You don't need to restart the server at all, just hit your site and again it will work!</p>
