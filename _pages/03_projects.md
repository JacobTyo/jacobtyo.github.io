---
layout: page
title: projects
permalink: /projects/
categories: core_page
---

<h1>projects</h1>
<h6>Some of the projects I have worked on.  This and project pages are incomplete.</h6>


<div id="projects" class="row mt-2 pt-3" style="overflow: visible !important;">
  {% for pages in site.pages %} 
  {% if pages.categories == "project_page" %}
  <div class="project-card">
  <a href="{{pages.permalink}}">
    <div class="card">
      <img class="card-img-top" src="{{site.baseurl}}{{pages.proj_pic}}" alt="project thumbnail" />
      <div class="card-body">
        <h5 class="card-title text-lowercase">{{pages.proj_title}}</h5>
        <p class="card-text">{{pages.proj_desc}}</p>
        <div class="row ml-1 mr-1 p-0">
        {% if pages.github_url != "" %}
          <div class="github-icon">
            <div class="icon" data-toggle="tooltip" title="Code Repository">
              <a href="{{pages.github_url}}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
            </div>
            <span class="stars" data-toggle="tooltip" title="GitHub Stars">
              <i class="fas fa-star"></i>
              <span id="tmp-stars"></span>
            </span>
          </div>
        {% endif %}
        </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %} 
  {% endfor %}
</div>