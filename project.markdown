---
layout: project
title: Projects
permalink: /project/
---

<div>
    {% for item in site.data.project %}
    <div class="project-card">
        <h1>{{ item.name }}</h1>
        <div>Technology used: {{ item.technology }} </div>
        <div>Documentation: {{ item.documentation }} </div>
        <div> {{ item.description }} </div>
        <a href="{{ item.demo }}"> Demo </a>
        <a href="{{ item.repository }}"> Repository </a>
    </div>
    {% endfor %}
</div>