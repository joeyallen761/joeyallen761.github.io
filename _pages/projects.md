---
layout: archive
title: "Projects HERE"
permalink: /projects/
author_profile: true
---
{% include base_path %}

{% for post in site.projects reversed %}
  {% include archive-single.html %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.excerpt }}</p>
{% endfor %}
