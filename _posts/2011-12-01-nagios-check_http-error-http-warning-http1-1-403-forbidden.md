---
title: 'Nagios CHECK_HTTP Error HTTP WARNING: HTTP/1.1 403 Forbidden'
date: 2011-12-01 15:01:45.000000000 -08:00
category: blog
tag:
- web
- check_http
- http
- nagios
---
<p>So, I was deploying a new server and added the default CHECK_HTTP Nagios plug-in as follows:</p>
<p><code><br />
define service{<br />
        use
<preset service type>
        host_name                       <server name><br />
        service_description             HTTP<br />
        check_command                   check_http<br />
        }<br />
</server></preset></code></p>
<p>However, the check would come back as an 403 Forbidden error. I know we have some restrictions set on our http.conf to allow only internal IP addresses to the Apache server, but the Nagios server is in the internal network. Poked around the settings and configurations for awhile and could not see any issues as I was able to browse the default Apache page.</p>
<p>Looked a bit more and found that the CHECK_HTTP is actually looking for an index page in the root html location. So I ended up creating a dummy page for Nagios and the checks came back fine! I'm sure you could make something nicer but this is all I did in the /var/www/html directory:</p>
<p><code><br />
echo "This is a dummy page for <server name>." >> index.html<br />
</server></code></p>
<p>Works like a charm!</p>
