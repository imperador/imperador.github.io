---
layout: page
title: projects
permalink: /projects/
description: some of the projects I have worked on
---

<div id="projects" class="card-columns mt-2 mr-4 pt-3" style="overflow: visible !important;">
  {% for project in site.projects %}
    {% if project.redirect %}
      <a href="{{ project.redirect }}" target="_blank">
    {% else %}
      <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
    {% endif %}
      <div class="card hoverable m-3 p-0 col" style="display: inline-block; overflow: visible !important;">
        <img class="card-img-top" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}" alt="project thumbnail">
        <div class="card-body" style="border-top: 1px solid rgba(60, 72, 88, 0.2);">
          <h5 class="card-title text-lowercase">{{ project.title }}</h5>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
              <div class="project-icon mr-1">
                <a href="{{ project.github }}" target="_blank"><i class="fa fa-github gh-icon"></i></a>
              </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  {% endfor %}
</div>
