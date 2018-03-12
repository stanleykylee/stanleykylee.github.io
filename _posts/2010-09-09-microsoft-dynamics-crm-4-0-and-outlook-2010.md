---
title: Microsoft Dynamics CRM 4.0 and Outlook 2010
date: 2010-09-09 09:30:51.000000000 -07:00
category: blog
tag:
- work
- CRM
---
<p>Although both products are from Microsoft, they don't seem to play nice together. Most likely due to the fact Office 2010 came out recently and has changed the way it interacts with the system. Either way, when installing CRM the following error showed up:</p>
<blockquote><p>(Error) Setup failed to determine whether a supported version of Microsoft Outlook is installed</p></blockquote>
<p>The only solution is the ignore this manually. To do so, create the following into the registry (the entry does not yet exist):</p>
<p><code>[HKEY_CURRENT_USER \ SOFTWARE \ Microsoft \MSCRMClient]<br />
Key Type: DWORD<br />
Key: IgnoreChecks<br />
Value: 1</code></p>
<p>The installer will still state the error but it will now allow you to continue with the install! Good luck!</p>
<p>Reader suggests the following command instead of clicking around the registry:</p>
<p><code>reg add HKCU\Software\Microsoft\MSCRMClient /v IgnoreChecks /t REG_DWORD /d 1</code></p>
