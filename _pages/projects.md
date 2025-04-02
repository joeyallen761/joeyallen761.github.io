---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---
{% include base_path %}

{% for post in site.projects reversed %}
  <img src="{{ post.image }}" alt="{{ post.title }} image" style="max-width:200px;">
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.excerpt }}</p>
{% endfor %}
