---
layout: page
permalink: /teaching/
title: teaching
nav: teaching
description: classes, workshops, and teaching material
---

<div class="teaching">
        {% for entry in site.data.teaching %}
            <h3 class="mt-4">{{ entry.title }}</h3>
            {% for course in entry.courses %}
                <div class="card mt-3 p-3">
                    <div class="row">
                        <div class="col-sm-10">
                            <h5 class="title font-weight-bold">{{course.coursename}}</h5>
                        </div>
                        <div class="col-sm-2 text-left text-sm-right" style="min-width: 75px;">
                            <span class="badge font-weight-bold danger-color-dark text-uppercase align-middle" style="min-width: 75px;">
                                {{course.coursenumber}}
                            </span>
                        </div>
                    </div>
                    <h6 class="font-italic mt-2 mt-sm-0">{{course.teaching}}</h6>
                    <div>
                    <ul class="card-text font-weight-light list-group list-group-flush">
                            <li class="list-group-item" style="border-top: 1px solid #ddd;">
                                <div class="row"> 
                                <h6 class="ml-1 ml-md-4">
                                    {{course.description}}
                                </h6>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            {%endfor%}
        {% endfor %}
        </div>