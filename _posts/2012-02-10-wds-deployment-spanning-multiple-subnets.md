---
title: WDS Deployment spanning multiple subnets
date: 2012-02-10 11:00:14.000000000 -08:00
category: blog
tag:
- work
- CentOS
- Cisco
- DHCP
- WDS
---
<p>This turned out to be simpler than I had first imagined. Reading the Microsoft documentation looked like we had to make changes to the DHCP, however this was not the case.</p>
<p>To make it clearer, our current environment looks like this:</p>
<ol>
<li>DHCP is a Linux CentOS Server</li>
<li>WDS and DHCP servers are on the same subnet</li>
<li>Client machines are on various subnets</li>
<li>Cisco core switch and router stack</li>
</ol>
<p>For our setup, we only needed to make sure the Cisco ip helper-address was set to point to the IP address of BOTH the DHCP and WDS. Once this was done, everything went as intended.</p>
