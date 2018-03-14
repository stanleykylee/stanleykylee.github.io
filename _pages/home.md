---
permalink: /
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/home-page-feature-water.jpg
  caption:
excerpt: 'another technology blog, because sharing is caring'
---

<h2>Latest Post</h2>
{% for post in site.posts limit:1 %}
  {% include archive-single.html %}
{% endfor %}
<h2>Recent Posts</h2>
{% for post in site.posts offset:1 limit:4 %}
  {% include archive-single.html %}
{% endfor %}