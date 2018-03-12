---
title: A bug in Bugzilla 4.0.4
date: 2012-02-13 14:01:38.000000000 -08:00
category: blog
tag:
- work
- bugzilla
- CPAN
- perl
- YAML
---
<p>There was a request to have a new tool custom report tool created for our Bugzilla installation so I had to re-deploy a copy of Bugzilla onto our development environment. Installation was a bit tricky with a specific Perl module (YAML) being the main issue. The install script keeps saying that this is missing:</p>
<p><code>Checking for                 YAML (any)       not found</code></p>
<p>Checking the system, YAML is indeed installed and available. What is actually broken is the CPAN.pm file in the Bugzilla package - it doesn't require the module.</p>
<p>To fix this, add the YAML module into the CPAN.pm file found in the bugzilla/lib directory. Search for:</p>
<p><code>use Text::Wrap ();</code></p>
<p>And replace with:</p>
<p><code>use Text::Wrap ();<br />
use YAML;</code></p>
<p>Running the install script now works with no errors.</p>
