---
title: Failure to start new MySQL server
date: 2011-12-22 10:29:06.000000000 -08:00
category: blog
tag:
- work
- mysql
---
<p>We use replication for our MySQL server and perform a snapshot rsync to re-initialize the slave servers. One difference today was that I had to create a whole new server from scratch and perform the same re-initialization. Everything worked fine until I tried to start the server:</p>
<blockquote><p>Fatal error: Can’t open and lock privilege tables: Table ‘mysql.host’ doesn’t exist</p></blockquote>
<p>The server was new and had not been initialized yet. I had copied all the data files including the my.cnf files and had expected the MySQLd to work! Well, doesn't always happen that way eh?</p>
<p>Anyways, all that I had to do was to tell MySQLd where the data is located:</p>
<p><code>mysql_install_db –user=mysql –ldata=/<em>datadir in my.cnf</em></code></p>
<p>MySQL came up and is replicating again!</p>
