---
title: Scripting DROP SYNONYM
date: 2013-03-20 08:15:40.000000000 -07:00
category: blog
tag:
- work
- SQL Server
---
<p>Recently we needed to refresh our test database and the synonyms in the test environment is different from the production environment. Instead of re-creating all the synonyms one-by-one, this task can be semi-automated.</p>
<ol>
<li>Run the following code on the old production database<br />
<code><br />
SET NoCount ON  -- optional<br />
SELECT DISTINCT 'DROP SYNONYM [' + SCH.name + '].' + SYN.name<br />
FROM<br />
  Sys.Synonyms SYN<br />
JOIN<br />
  Sys.Schemas SCH ON SYN.schema_id = SCH.schema_id<br />
WHERE<br />
   SYN.is_ms_shipped = 0<br />
SET NoCount OFF  -- optional<br />
</code></li>
<li>Verify the synonyms to be deleted and copy the resulting DROP statements into a new query table</li>
<li>Right-click the database and select Tasks<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/tasks.jpg"><img src="{{ site.baseurl }}/assets/images/tasks.jpg" alt="tasks" width="194" height="304" class="alignnone size-full wp-image-338" /></a></li>
<li>Select Generate Scripts<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/generate_scripts.jpg"><img src="{{ site.baseurl }}/assets/images/generate_scripts.jpg" alt="generate_scripts" width="254" height="420" class="alignnone size-full wp-image-337" /></a></li>
<li>Select Next<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/gs_step1.jpg"><img src="{{ site.baseurl }}/assets/images/gs_step1.jpg" alt="gs_step1" width="721" height="666" class="alignnone size-full wp-image-340" /></a></li>
<li>Select Synonyms and then Next<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/gs_step2.jpg"><img src="{{ site.baseurl }}/assets/images/gs_step2.jpg" alt="gs_step2" width="721" height="666" class="alignnone size-full wp-image-341" /></a></li>
<li>Select Save to Clipboard (or you can save to file)<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/gs_step3.jpg"><img src="{{ site.baseurl }}/assets/images/gs_step3.jpg" alt="gs_step3" width="721" height="666" class="alignnone size-full wp-image-342" /></a>
	</li>
<li>Confirm the Server and Database. Select Next<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/gs_step4.jpg"><img src="{{ site.baseurl }}/assets/images/gs_step4.jpg" alt="gs_step4" width="721" height="666" class="alignnone size-full wp-image-343" /></a></li>
<li>Select Finish<br />
<a href="http://stanleylee.hk/wp-content/uploads/2013/03/gs_step5.jpg"><img src="{{ site.baseurl }}/assets/images/gs_step5.jpg" alt="gs_step5" width="721" height="666" class="alignnone size-full wp-image-344" /></a></li>
<li>Paste the create synonyms queries into the previous query window.</li>
<li>Run on the newly restored development database</li>
</ol>
