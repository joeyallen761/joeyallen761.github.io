---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---
{% include base_path %}

{% for post in site.projects %}
<div class="project-preview">
  <img src="{{ post.image }}" alt="{{ post.title }} image">
  <div class="project-text">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </div>
</div>
{% endfor %}
