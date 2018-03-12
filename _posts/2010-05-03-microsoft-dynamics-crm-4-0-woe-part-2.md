---
title: Microsoft Dynamics CRM 4.0 woe part 2
date: 2010-05-03 20:49:01.000000000 -07:00
category: blog
tag:
- work
- CRM
---
<p>Microsoft Dynamics CRM, this is truly a beast of a software. Installation is often a hit or miss based on what is currently installed on the PC.</p>
<p>Recently I had to install CRM onto a PC plagued with problems. There were updates for Windows, software half installed and remaining files from previously installed software. To add to that the PC was at a remote location and required a VPN connection back to the main office. Refer to my other <a href="http://stanleylee.hk/2010/04/30/crm-4-0-dynamics-woe" target="_blank">posting</a> to see how that was resolved.</p>
<p>Thinking that I had resolved the problem, I had left the user to the PC - boy was I wrong. CRM did not like the fact that I had previously logged into that PC with my account (when I was foolishly testing it). Basically, the CRM checks if there is already an user installed into the SQL server and if there is, CRM will not allow another user. Attempting to resolve this by removing the data proved to be a futile effort. I basically had to uninstall everything including CRM and the SQL Server to allow the user to register himself on Outlook with the CRM plugin.</p>
<p>Hopefully, this time around, the issue is finally laid to rest!</p>
