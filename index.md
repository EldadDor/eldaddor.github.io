---
layout: tabbed
title: Eldad Dor - Resume
about_content: |
  Senior Java Technical Lead & DevOps Engineer with <mark>15+ years of experience</mark> delivering scalable enterprise solutions. Since 2023, embedded in the DevOps team while leading Java modernization initiatives, CI/CD automation, and platform operations.
  
  Expertise in microservices architecture, containerization, and AI-assisted engineering. Recognized for driving developer productivity through tooling innovation, clean code practices, and comprehensive automation strategies.
---

{% for section in site.content %}
  <div class="resume-section">
    <h2>{{ section.title }}</h2>
    {% if section.layout == "list" %}
      {% for item in section.content %}
        <div class="list-item">
          <h3>{{ item.title }}</h3>
          <h4>{{ item.sub_title }}</h4>
          <p class="caption">{{ item.caption }}</p>
          {{ item.description | markdownify }}
        </div>
      {% endfor %}
    {% elsif section.layout == "text" %}
      {{ section.content | markdownify }}
    {% endif %}
  </div>
{% endfor %}
