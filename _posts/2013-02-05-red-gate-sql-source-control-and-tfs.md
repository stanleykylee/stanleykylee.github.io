---
title: Red Gate SQL Source Control and TFS
date: 2013-02-05 17:02:56.000000000 -08:00
category: blog
tag:
- work
- proxy
- redgate
- sql source control
- tfs
---
<p>We currently use RedGate SQL Source Control and TFS for our source control. However, for some reason, there was some changes made somewhere which caused all our developer's SQL Source Control to halt  while continually trying to complete step 2 of 4. It displayed a message saying:</p>
<blockquote><p>Determining latest version</p></blockquote>
<p>After a thorough investigation, it was narrowed down to our current firewall and proxy settings. As we use an authentication require web proxy, the application was not forwarding the credentials properly.</p>
<p>We included two exemptions for the red-gate.com site and our users were able to update the software. After updating the software, the developers were able to check in changes and contacted TFS with no further issues!</p>
