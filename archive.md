---
layout: page
title: Archive
permalink: /archive/
sitemap:
  lastmod: 2014-01-23
  priority: 0.7
  changefreq: 'monthly'
  exclude: 'yes'
---

{% for post in site.posts %}
  * {{ post.date | date_to_string }}:  [ {{ post.title }} ]({{ post.url }})
{% endfor %}

##Projects

{% assign projects = (site.pages | where: "layout" , "project") %}
{% for page in projects %}
 * [ {{ page.title }} ]({{ page.url }})  
{% endfor %}


<!-- <nav><ul>
{% for node in site.pages %}
	{% if node.title != nil and node.url != '/' %}
	{% capture nodediff %}{{ page.url | remove:node.url }}{% endcapture %}
	<li><a {% if nodediff != page.url %}class="active" {% endif %}href="{{ node.url }}">{{ node.title }}</a></li>
	{% endif %}
{% endfor %}
</ul></nav> -->

