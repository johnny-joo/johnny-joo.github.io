---
layout: page
title: Awards & Competitions
permalink: /awards/
---

## Awards & Recognition

A showcase of competitions, hackathons, and awards that I've participated in and won. Each experience has contributed to my growth and learning.

<div class="awards-list">
{% for award in site.awards %}
  <article class="award-item">
    <h3><a href="{{ award.url | relative_url }}">{{ award.title }}</a></h3>
    <p class="award-meta">
      <span class="position">{{ award.position }}</span> | 
      <span class="date">{{ award.date | date: "%B %Y" }}</span>
    </p>
    <p class="organizer">{{ award.organizer }}</p>
    <p class="description">{{ award.excerpt | strip_html | truncatewords: 40 }}</p>
    <a href="{{ award.url | relative_url }}" class="read-more">Read More →</a>
  </article>
{% endfor %}
</div>

{% if site.awards.size == 0 %}
<p>No awards listed yet. Check back soon!</p>
{% endif %}

---

## Categories

- **🏆 Hackathons:** Competitive coding and innovation challenges
- **🎯 Competitions:** Business plans, design contests, and more
- **🌟 Recognition:** Scholarships, certifications, and honors
- **🚀 Innovation:** Awards for creative solutions and technologies

## Skills Demonstrated

Through these competitions, I've developed and demonstrated:
- Problem-solving under pressure
- Team collaboration and leadership
- Rapid prototyping and development
- Presentation and communication skills
- Innovation and creative thinking
