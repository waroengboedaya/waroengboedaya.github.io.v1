---
layout: page
title: 
permalink: 
---
*We are a small, casual company who have fond interest on design and craftmanship as way of  life. We explore, learn and build with our head, heart and hands. We cherish creating works that brings joy and meaning in everyday’s life and community we live in. These are some of works we've done:*

{% assign pages = site.pages | sort: 'date' | reverse %}
{% for page in pages %}
{% if page.resource == true %}
{% for pc in page.categories %}
{% if pc == "featured" %}
<div class="post">
<a href="{{ page.url | prepend: site.baseurl }}" class="post-link">
<h3 class="post-title">{{ page.title }}</h3>
<p class="post-summary">{% if page.achievement %} <small><em>{{ page.achievement}}</em></small><br/>  {% endif %} {{ page.summary }}  </p>
</a>
</div>
{% endif %}  
{% endfor %}  
{% endif %}  
{% endfor %} 

