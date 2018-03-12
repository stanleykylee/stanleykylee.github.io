---
title: Niceness and Renice
date: 2010-06-13 23:14:28.000000000 -07:00
category: blog
tag:
- work
- linux
---
<p>So I was playing around with streaming media to my PS3 and came to a problem. My NAS running on Linux was running several items at the same time. Most noticeably is bit torrent and an internal site (Apache and MySQL). Due to this, streaming was stuttering and disconnecting randomly. It also produced an "dlna protocol error 2006" on the PS3.</p>
<p>Digging around I found that the default nice level for the DLNA process was set to 19. Think of the nice level as the priority, with -20 the highest and 19 the lowest. Most definitely this will cause problems with so many processes running!</p>
<p>Started the top command and found all the DLNA processes after sorting the results and ran the renice command:</p>
<blockquote><p>renice -5 -p pid</p></blockquote>
<p>This re-prioritiezed the DLNA processes to be at a much higher priority. With that, the problem went away!</p>
<p>Once again, have fun!</p>
