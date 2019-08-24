---
layout: page
title: projects
nav: projects
permalink: /projects/
description: some of the projects I have worked on
---

<div id="projects" class="row mt-2 pt-3" style="overflow: visible !important;">
  {% assign sorted_projects = site.projects | sort: "importance" | reverse %}
  {% for project in sorted_projects %}
    <div class="col-12 col-sm-6 col-md-4">
      {% if project.redirect %}
        <a href="{{ project.redirect }}" target="_blank">
      {% else %}
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
      {% endif %}
        <div class="card hoverable mb-4 p-0" style="display: inline-block; overflow: visible !important;">
          <img class="card-img-top" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}" alt="project thumbnail">
          <div class="card-body" style="border-top: 1px solid rgba(60, 72, 88, 0.2);">
            <h5 class="card-title text-lowercase">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <div class="row ml-1 mr-1 p-0">
              {% if project.wordpress %}
                <div class="mt-2 ml-n1 mr-2 p-0" data-toggle="tooltip" title="Blog Post">
                  <div class="project-icon mr-1">
                    <a href="{{ project.wordpress }}" target="_blank"><i class="fab fa-wordpress-simple wp-icon"></i></a>
                  </div>
                </div>
              {% endif %}
              {% if project.github %}
                {% assign github_id = project.title | append: project.github | replace: '/', '-' | replace: ' ', '-' %}
                <div class="mb-n4 mt-2 ml-n1 mr-2 p-0">
                  <div class="project-icon mr-1" data-toggle="tooltip" title="Code Repository">
                    <a href="https://github.com/{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
                  </div>
                  <span class="badge badge-danger badge-notify" data-toggle="tooltip" title="GitHub Stars">
                    <i class="fas fa-star"></i>
                    <span id="{{ github_id }}-stars"></span>
                  </span>
                </div>
              {% endif %}
            </div>
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>
