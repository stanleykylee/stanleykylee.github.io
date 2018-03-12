---
title: MySQL database restoration error
date: 2010-05-06 09:35:45.000000000 -07:00
category: blog
tag:
- work
- mysql
---
<p>So I was trying to restore a backup database from a .sql file through the following command:</p>
<blockquote><p>mysql <em>database</em> &lt; <em>file.sql</em></p></blockquote>
<p>And an error resulted:</p>
<blockquote><p>Got a packet bigger than 'max_allowed_packet' bytes</p></blockquote>
<p>This is most likely due to the fact that there are large images and other files in the database causing problems. I had to edit the MySQL configuration files and added the following:</p>
<blockquote><p>vim /etc/my.cnf</p>
<p>set-variable=max_allowed_packet=<em>x</em>M</p></blockquote>
<p>For my particular issue, I had to change <em>x</em> to 512. This may vary depending on how large your files are.</p>
