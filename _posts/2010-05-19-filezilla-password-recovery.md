---
title: Filezilla password recovery
date: 2010-05-19 09:58:57.000000000 -07:00
category: blog
tag:
- work
- filezilla
---
<p>Recently I had to recover passwords from a dead windows installation. Be it good or bad, Filezilla stores its passwords in plain text! I was able to get all my sites, but users should be aware that the passwords are in no safe from prying eyes...</p>
<p>The following files are what you need to know about:</p>
<blockquote><p>filezilla.xml – Stores most recent server info including password in plaintext.<br />
recentservers.xml – Stores all recent server info including password in plaintext.<br />
sitemanager.xml – Stores all saved sites server info including password in plaintext.</p></blockquote>
<p>These files can usually be found in the following directories:</p>
<blockquote><p>Windows XP/2K: “C:\Documents and Settings\username\Application Data\FileZilla”<br />
Windows Vista: “C:\Users\username\AppData\Roaming\FileZilla\”<br />
Linux: “/home/username/.filezilla/”</p></blockquote>
