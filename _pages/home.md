---
layout: splash
permalink: /
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/home-page-feature-water.jpg
  caption:
excerpt: 'another technology blog, because sharing is caring'
intro:
  - excerpt: '[<i class="fab fa-twitter"></i>](https://twitter.com/stanleykylee){: .btn .btn--twitter} [<i class="fab fa-github"></i>](https://github.com/stanleykylee){: .btn .btn--github} [<i class="fab fa-linkedin"></i>](https://linkedin.com/in/stanleykylee){: .btn .btn--linkedin}'
---

{% include feature_row id="intro" type="center" %}

{% for post in site.posts limit:10 %}
  {% include archive-single.html %}
{% endfor %}