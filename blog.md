---
layout: page
title: Blog
permalink: /blog/
---

## Latest Posts

<div class="blog-posts">
{% for post in site.posts %}
  <article class="post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">
      <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
      {% if post.author %}
      <span class="author">by {{ post.author }}</span>
      {% endif %}
    </p>
    <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    <div class="tags">
      {% for tag in post.tags %}
      <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
  </article>
{% endfor %}
</div>

{% if site.posts.size == 0 %}
<p>No blog posts yet. Check back soon!</p>
{% endif %}

---

## About This Blog

This blog is where I share my thoughts, tutorials, and insights on [Your Topics of Interest]. Topics include:

- Technical tutorials and guides
- Project retrospectives and lessons learned
- Industry trends and analysis
- Personal development and career growth

Subscribe via [RSS](/feed.xml) to stay updated!
