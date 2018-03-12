---
title: VMware vSphere Client cannot mount local optical drive
date: 2012-02-06 14:44:51.000000000 -08:00
category: blog
tag:
- work
- permissions
- VMware
- vSphere Client
- Windows 7
---
<p>Another quick post regarding a nagging issue I've had for awhile now. Every time I wanted to connect to my local optical drive it would complain with the following error immediately:</p>
<p><code>Remote device disconnect<br />
The remote device on <host> connected to
<path> is disconnected.</path></host></code></p>
<p>Digging around I found that the cause of this is because of Windows 7 permissions again. Running the application as Administrator or checking off the "Run this program as an administrator" under the Compatibility tab of the vSphere Client shortcut solved the issue!</p>
<p>Hope this helps you all as well.</p>
