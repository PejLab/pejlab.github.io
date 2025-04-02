---
layout: page
title: Tools and Data
permalink: /tools-and-data/
---

<div class="github-link">
  <a href="https://github.com/PejLab" target="_blank" rel="noopener noreferrer">
    <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg>
    Visit our GitHub
  </a>
</div>

<div class="projects-grid">
{% for project in site.data.projects %}
  <div class="project-card">
    {% if project.image %}
      <img src="/assets/images/projects/{{ project.image }}" alt="{{ project.name }}" class="project-image">
    {% endif %}
    <div class="project-content">
      <h3 class="project-title">{{ project.name }}</h3>
      <p class="project-description">{{ project.description }}</p>
      <div class="project-links">
        {% for link in project.links %}
          <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer">
          {{ link.name }}
          </a>{% unless forloop.last %} • {% endunless %}
        {% endfor %}
    </div>
    </div>
  </div>
{% endfor %}
</div>

<style>
.github-link {
  /* text-align: center; */
  margin-bottom: 2rem;
}

.github-link a {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background-color: #24292e;
  color: white;
  text-decoration: none;
  border-radius: 6px;
  transition: background-color 0.2s;
}

.github-link a:hover {
  background-color: #2f363d;
}

.projects-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
}

.project-card {
  border: 1px solid #d1d4d8;
  border-radius: 8px;
  background-color: #ffffff;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: contain;
}

.project-content {
  padding: 1rem;
}

@media (min-width: 768px) {
  .project-card {
    flex-direction: row;
  }
  
  .project-image {
    width: 200px;
    height: auto;
  }
  
  .project-content {
    flex: 1;
  }
}

</style>
