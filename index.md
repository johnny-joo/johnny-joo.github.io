---
layout: default
title: Home
---

<div class="home">
  <section class="hero">
    <h1>Welcome to My Portfolio</h1>
    <p class="lead">Hi! I'm [Your Name], a [Your Role/Title]</p>
    <p>I'm passionate about [Your Interests/Expertise]. This portfolio showcases my projects, achievements, and professional journey.</p>
  </section>

  <section class="highlights">
    <h2>Highlights</h2>
    <div class="highlight-grid">
      <div class="highlight-item">
        <h3>🏆 Awards</h3>
        <p>Multiple competition wins and recognitions</p>
        <a href="{{ '/awards/' | relative_url }}" class="btn">View Awards</a>
      </div>
      <div class="highlight-item">
        <h3>💼 Projects</h3>
        <p>Innovative solutions and creative works</p>
        <a href="{{ '/projects/' | relative_url }}" class="btn">View Projects</a>
      </div>
      <div class="highlight-item">
        <h3>✍️ Blog</h3>
        <p>Thoughts, tutorials, and insights</p>
        <a href="{{ '/blog/' | relative_url }}" class="btn">Read Blog</a>
      </div>
    </div>
  </section>

  <section class="recent-projects">
    <h2>Recent Projects</h2>
    <div class="project-list">
      {% for project in site.projects limit:3 %}
      <article class="project-card">
        <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
        <p class="meta">{{ project.date | date: "%B %Y" }} | {{ project.category }}</p>
        <p>{{ project.excerpt | strip_html | truncatewords: 30 }}</p>
        <a href="{{ project.url | relative_url }}">Read more →</a>
      </article>
      {% endfor %}
    </div>
  </section>

  <section class="recent-posts">
    <h2>Latest Blog Posts</h2>
    <ul class="post-list">
      {% for post in site.posts limit:3 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
      </li>
      {% endfor %}
    </ul>
  </section>
</div>
