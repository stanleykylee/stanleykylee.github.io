---
title: Moving MS databases from one server to another
date: 2013-01-11 16:58:45.000000000 -08:00
category: blog
tag:
- work
- attach
- detach
- orphaned users
- SQL Server
---
<p>Deployed a new test server to replace an aging development server. Aside from the set up and other technical requirements, we needed to move the data from the old MSSQL server to the new MSSQL server. Quick steps to do so:</p>
<p>1. Make note of current location of database files.</p>
<p><a href="http://stanleylee.hk/2013/01/11/moving-ms-databases-from-one-server-to-another/select_properties/" rel="attachment wp-att-205"><img src="{{ site.baseurl }}/assets/images/select_properties-263x300.jpg" alt="select_properties" width="263" height="300" class="alignnone size-medium wp-image-205" /></a></p>
<p><a href="http://stanleylee.hk/wp-content/uploads/2013/01/properties_panel.jpg"><img src="{{ site.baseurl }}/assets/images/properties_panel.jpg" alt="properties_panel" width="704" height="632" class="alignnone size-full wp-image-268" /></a></p>
<p>2. Detach database from old server. Ensure that you select option to disconnect active connections.</p>
<p><a href="http://stanleylee.hk/2013/01/11/moving-ms-databases-from-one-server-to-another/detach/" rel="attachment wp-att-210"><img src="{{ site.baseurl }}/assets/images/detach-300x94.jpg" alt="detach" width="300" height="94" class="alignnone size-medium wp-image-210" /></a></p>
<p>3. Move the files to the new server. Make note of the location of the files after moving them to the new server. This will required when attaching the database to the new server. You may also need to manually select the location of the log file for the database.</p>
<p><a href="http://stanleylee.hk/2013/01/11/moving-ms-databases-from-one-server-to-another/attach/" rel="attachment wp-att-207"><img src="{{ site.baseurl }}/assets/images/attach.jpg" alt="attach" width="275" height="59" class="alignnone size-full wp-image-207" /></a></p>
<p><a href="http://stanleylee.hk/2013/01/11/moving-ms-databases-from-one-server-to-another/attach_select/" rel="attachment wp-att-208"><img src="{{ site.baseurl }}/assets/images/attach_select.jpg" alt="attach_select" width="704" height="632" class="alignnone size-full wp-image-208" /></a></p>
<p>4. Once the database is attached to the new server, check for any orphaned users.</p>
<p><code>sp_change_users_login 'report'</code></p>
<p>5. If there are any users listed in the report above, you can fix them with the following command. Replace %user% with the name of your user listed in the above report. Make note to keep the single quotations.</p>
<p><code>sp_change_users_login 'auto_fix', '<em><<user>></user></em>'</code></p>
<p>Done!</p>
