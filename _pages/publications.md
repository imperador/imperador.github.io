---
layout: page
permalink: /publications/
title: publications
nav: publications
description: <span>*</span> denotes equal contribution and joint lead authorship.
years: [2021, 2020, 2019]
---

<br/>
{% for y in page.years %}
  <div class="row m-0 p-0" style="border-top: 1px solid #ddd; flex-direction: row-reverse;">
    <div class="col-sm-1 mt-2 p-0 pr-1">
      <h3 class="bibliography-year">{{y}}</h3>
    </div>
    <div class="col-sm-11 p-0">
      {% bibliography -f papers -q @*[year={{y}}]* %}
    </div>
  </div>
{% endfor %}

<div class="whitep mt-3 p-0">
  <h3 class="title mt-2 p-0">other</h3>
  A list of white papers, technical reports and other non peer-reviewed publications<br/><br/>
  {% assign whitep = site.whitep | reverse %}
  {% for item in whitep %}
    <div class="row p-0">
      <div class="col-sm-1 p-0">
        <span class="badge danger-color-dark font-weight-bold text-uppercase align-middle ml-3">
          {{ item.type | type }}
        </span>
      </div>
      <div class="col-sm-11 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 pl-xs-0 pl-sm-4 pr-sm-2 font-weight-light text"> 
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>