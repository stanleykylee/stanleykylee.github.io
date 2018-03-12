---
title: Force feeding Windows Server 2003
date: 2010-06-16 16:29:12.000000000 -07:00
category: blog
tag:
- work
- windows server 2003
---
<p>Another day at work, another interesting problem. A user was connecting to a terminal server and tried to print to a printer that was installed locally on her PC. Logging into the terminal server via RDC showed no printers available.</p>
<p>First step was to ensure that the printer was a shared local resource. This was alright, however the printer still does not want to show up. Frustrated, I tried to install the printer locally by downloading the printer drivers on the terminal server. Running the install file did nothing so I had to find another way to force the drivers onto the system.</p>
<p>Logging onto the terminal server as Administrator, I found a way to trick the server and force feed it the drivers.</p>
<ol>
<li>Enter into the control panel and install a new local printer. Install manually and do not search for a printer.</li>
<li>Select a printer port to be "FILE: (Print to File)" and choose your own printer drivers (select have disk).</li>
<li>From the downloaded driver file, select the INF or if it is already in the list of available drivers, select your printer from there.</li>
<li>Continue through with the installation and allow the printer to be installed. Remember to name it something random as this is only temporary and you will delete this printer after.</li>
<li>Once the dummy print to file printer is installed, log off the terminal server and re-log back in.</li>
<li>As you log in, you will notice that Windows has now installed the printer that was having troubles.</li>
<li>Remove the dummy printer so that it doesn't show up in the printer list!</li>
</ol>
<p>So, that's what I did to make this work. You can also check in the system logs to see that whether or not this method is necessary. In the system log, you will see an 1111 error code stating that the printer driver could not be found and the printer was not installed.</p>
<p>Hope this helps!</p>
