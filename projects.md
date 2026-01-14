---
layout: page
title: Projects
permalink: /projects/
---

## My Projects

Here's a collection of projects I've worked on, ranging from personal experiments to professional work. Each project represents a learning journey and showcases different skills and technologies.

<div class="projects-grid">
{% for project in site.projects %}
  <article class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    <p class="meta">
      <span class="date">{{ project.date | date: "%B %Y" }}</span>
      {% if project.category %}
      <span class="category">{{ project.category }}</span>
      {% endif %}
    </p>
    <p class="description">{{ project.excerpt | strip_html | truncatewords: 30 }}</p>
    <div class="tags">
      {% for tag in project.tags %}
      <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    <a href="{{ project.url | relative_url }}" class="read-more">View Project →</a>
  </article>
{% endfor %}
</div>

{% if site.projects.size == 0 %}
<p>No projects yet. Check back soon!</p>
{% endif %}

---

## Project Categories

- **Web Development:** Full-stack applications and websites
- **Data Science:** Machine learning and data analysis projects
- **Mobile Apps:** iOS and Android applications
- **Open Source:** Contributions to open-source projects
- **Research:** Academic and experimental projects

### Want to Collaborate?

I'm always interested in working on exciting projects. If you have an idea or want to collaborate, [get in touch](/about/)!
