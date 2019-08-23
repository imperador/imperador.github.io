---
layout: page
permalink: /publications/
title: publications
<!-- description: <em class="star">*</em> denotes equal contribution and joint lead authorship. -->
years: [2019, 2018, 2017, 2016, 2015, 2014, 2012]
---

{% for y in page.years %}
  <div class="row" style="border-bottom: 1px solid #ddd;">
    <div class="col-sm-10">
      {% bibliography -f papers -q @*[year={{y}}]* %}
    </div>
    <div class="col-sm-2 align-self-end">
      <h3 class="bibliography-year pt-2">{{y}}</h3>
    </div>
  </div>
{% endfor %}
