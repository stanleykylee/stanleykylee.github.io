---
title: CRM 4.0 Dynamics woe
date: 2010-04-30 01:15:41.000000000 -07:00
category: blog
tag:
- work
- CRM
- MSXML
---
<p>Working on another PC, I am came across issues with CRM. Basically, it would not install due to the fact that that I was installing the 'offline version'. The only thing that showed up on the install was:</p>
<blockquote><p>Microsoft SQL Server 2005 Express Edition (CRM) - Installation Failed</p></blockquote>
<p>With no hints at hand, I had to search around to see what was wrong. The CRM installation was less than helpful as it did not provide any further details regarding this error. However, an eureka moment occurred! Could this be the same error I was receiving with the massive Windows Updates failures I was trying to deal with last week?</p>
<p>So, I took a stab to look through the list of programs installed and sure enough, MSXML6 was installed. Previously, Microsoft SQL Server updates were failing because MSXML6 update was installed, the removal of this patch allowed the Microsoft SQL Server to install properly.</p>
<p>Happily I thought I could just remove it and reinstall, but of course, there had to be a catch! Simply clicking remove from the Add / Remove Programs (in Control Panel) did nothing - uninstall failed. Argh! So back to the drawing board!</p>
<p>After more research, it turns out that this is a not an uncommon problem for programs to not uninstall properly. Microsoft has even created a tool to remedy this!</p>
<blockquote><p><a title="Windows Installer CleanUp Utility" href="http://support.microsoft.com/kb/290301" target="_blank">Windows Installer CleanUp Utility</a></p></blockquote>
<p>After installing the tool, removing MSXML6, I was able to continue with the install of CRM! Got the user to log in, setup the CRM settings to point to the correct server location and off we go!</p>
<p>Another issue resolved...</p>
