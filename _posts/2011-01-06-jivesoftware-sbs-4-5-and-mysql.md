---
title: Jivesoftware - SBS 4.5 and MySQL
date: 2011-01-06 15:13:46.000000000 -08:00
category: blog
tag:
- work
- jive
- sbs
---
<p>It has been awhile, but I'm still alive. Anyway, installed SBS 4.5 from Jive Software today, however the JDBC for MySQL wasn't included in the installer.</p>
<p>Downloaded the files from the following link:<br />
<a href="http://dev.mysql.com/downloads/connector/j/">http://dev.mysql.com/downloads/connector/j/</a></p>
<p>Extracted the mysql-connector-java-5.1.12-bin.jar file (versions may be different as there are newer ones available) and copied it to the following folder:<br />
/usr/local/jive/tomcat/lib/</p>
<p>Restarted the Jive application and the connector worked!<br />
service jive-application restart</p>
<p>Hope that helps, and remember to have fun!</p>
