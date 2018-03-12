---
title: Making things go automagically
date: 2010-05-27 14:10:25.000000000 -07:00
category: blog
tag:
- work
- linux
---
<p>Was working away at work today and required to have a PERL script to be loaded every Friday. To do this, I had to employ the help of crontab.</p>
<p>usage:  crontab [-u user] file<br />
crontab [-u user] [ -e | -l | -r ]<br />
(default operation is replace, per 1003.2)<br />
-e      (edit user's crontab)<br />
-l      (list user's crontab)<br />
-r      (delete user's crontab)<br />
-i      (prompt before deleting user's crontab)<br />
-s      (selinux context)</p>
<ul type="disc">
<li>A minute, expressed as a number from 0 through 59.</li>
<li>An hour, expressed as a number from 0 through 23.</li>
<li>A day of the month, expressed as a number from 1 through 31.</li>
<li>A month of the year, expressed as a number from 1 through 12.</li>
<li>A day of the week, expressed as a number from 0 through 6 (with 0 standing for Sunday).</li>
</ul>
<p>Example of usage includes:</p>
<p>5 6 * * 1-5    <em>command</em><br />
10 8,14 * * 1-5  <em>command</em></p>
<p>There will always be 5 specifications. A static number, static numbers with commas in between, a range between numbers with a dash or an asterisk to represent all possible values.</p>
