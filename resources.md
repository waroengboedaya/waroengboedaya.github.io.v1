---
layout: page
title: Categories
permalink: /resources/
sitemap:
  lastmod: 2014-01-23
  priority: 0.7
  changefreq: 'monthly'
  exclude: 'yes'
---

{% for cat in site.category-list %}
### {{ cat | capitalize }}
<ul style="list-style:none; margin:0; padding:0">
{% for page in site.pages %}
{% if page.resource == true %}
{% for pc in page.categories %}
{% if pc == cat %}
<li> <div class="post">
<a href="{{ page.url | prepend: site.baseurl }}" class="post-link">
<h4 class="post-title">{{ page.title }}</h4>
<p class="post-summary">{{ page.summary }}  </p>
</a>
</div> </li>
{% endif %}   <!-- cat-match-p -->
{% endfor %}  <!-- page-category -->
{% endif %}   <!-- resource-p -->
{% endfor %}  <!-- page -->
</ul>
{% endfor %}
<!-- cat -->