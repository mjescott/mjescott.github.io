---
title: Blog
permalink: /blog/
layout: subpage
---

{% if site.posts.size > 0 %}
  <div class="blog-posts">
    {% for post in site.posts %}
      <div class="blog-card">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        
        <div class="post-meta">
          <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
          {% if post.author %}
            <span class="author"> • By {{ post.author }}</span>
          {% endif %}
        </div>
        
        <div class="excerpt">
          {{ post.excerpt | strip_html | truncate: 280 }}
        </div>
        
        <a href="{{ post.url | relative_url }}" class="read-more">Read more →</a>
      </div>
    {% endfor %}
  </div>

{% else %}
  <p>No blog posts yet. Come back soon!</p>
{% endif %}
