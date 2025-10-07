---
layout: page
title: "Projects"
permalink: /projects/
---
<div class="project-grid">
  {% for project in site.projects %}
  <div class="project-card">
    <a href="{{ project.url }}">
      {% if project.image %}
      <img src="{{ project.image }}" alt="{{ project.title }}">
      {% endif %}
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </a>
  </div>
  {% endfor %}
</div>

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}
.project-card {
  background: #1e1e1e;
  border-radius: 12px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.4);
}
.project-card img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 10px;
}
.project-card h3 {
  margin: 0.5em 0;
  color: #6ec1e4;
}
.project-card p {
  color: #ccc;
  font-size: 0.9em;
}
</style>
