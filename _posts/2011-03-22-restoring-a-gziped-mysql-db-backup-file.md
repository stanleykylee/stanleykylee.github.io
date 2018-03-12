---
title: Restoring a gziped MySQL DB backup file
date: 2011-03-22 11:34:52.000000000 -07:00
category: blog
tag:
- work
- gzip
- mysql
---
<p>Short post... just for reference:</p>
<p>gunzip < [backupfile.sql.gz] | mysql -u [uname] -p[pass] [dbname]</p>
