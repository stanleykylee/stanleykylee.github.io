---
title: VMware Conversion & Virtualization
date: 2010-04-27 22:40:44.000000000 -07:00
category: blog
tag:
- work
- multi-boot
- vCenter
- virtualization
- VMware
---
<p>So... I finally got the chance to update to Windows 7 and test out its new features to be able to provide support! However, I need to be able to access my old OS and any of the items in it. Since we were planning on supporting the Virtualization of PCs in the future as well, I thought to test it out on my PC.</p>
<p>Everything went smoothly except for one thing, there was an error:</p>
<blockquote><p>FAILED: Unable to find the system volume, reconfiguration is not possible.</p></blockquote>
<p>After some research, it turns out that the VMware vCenter Converter does not like any missing or irregular autoexec.bat, config.sys or boot.ini files. More specifically for me was the boot.ini as I had already installed Windows 7 in a dual boot mode. So I changed the boot.ini to:</p>
<blockquote><p>boot loader<br />
timeout=30<br />
default=multi(0)disk(0)rdisk(0)partition(1)\WINDOWS<br />
operating systems<br />
multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Windows XP Professional, Standard" /fastdetect</p></blockquote>
<p>Everything worked out fine after that. Now I'm happily using Windows 7 and running my XP programs and other items at the same time. True XP compatibilty mode!</p>
