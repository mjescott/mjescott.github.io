---
title: Blog
permalink: /blog/
layout: post
---

{% if site.posts.size > 0 %}

  {% for post in site.posts %}
    <article style="margin-bottom: 40px;">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html }}</p>
      <a href="{{ post.url | relative_url }}">Read more →</a>
    </article>
  {% endfor %}

{% else %}
  <p>No blog posts yet. Come back soon!</p>
{% endif %}
