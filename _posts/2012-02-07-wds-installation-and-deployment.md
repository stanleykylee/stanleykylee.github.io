---
title: WDS Installation and Deployment
date: 2012-02-07 14:02:24.000000000 -08:00
category: blog
tag:
- work
- WDS
---
<p>We're deploying a new WDS (Windows Deployment Service) server at work and at first everything looked alright until I ran into my first snag - I wasn't able to start the role / server after I installed it.</p>
<p>Looking everywhere on the manuals and guides provided by Microsoft didn't help either. All they say is to add the role to the server and then configure the server with deployment images etc.</p>
<p>Upon closer inspection, it seems like you need to initialize the server before it will even start. In order to do this, you need to run a command via an elevated command prompt window:</p>
<p><code>wdsutil.exe /initialize-server /reminst:
<path to wds data files /></code></p>
<p>I created my own folder for the WDS data files and then plugged that into the command. WDS started up with no further issues.</p>
<p>Next posting... how to get WDS to work with multiple subnets. I'll post that when I get it sorted out! :)</p>
