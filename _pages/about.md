---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD candidate studying HCI in the Computer Science Department at Washington University in St. Louis under the advisement of [Caitlin Kelleher](https://engineering.wustl.edu/faculty/Caitlin-Kelleher.html). My primary area of research examines the barriers that programmers face when collaborating across time and reusing code at a large scale. My work is aimed at developing both tools and guidelines to improve this process.

In addition to human-computer interaction, I am also interested in the interaction of technology and society--how can we use tech to improve the world, and what can go wrong along the way?

If any of these topics are interesting to you, please don't hesitate to reach out via e-mail! I would love to learn about more people, projects, and ideas in this space.

## Projects
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

## Publications
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
