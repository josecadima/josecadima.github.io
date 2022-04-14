---
layout: project
title: Projects
permalink: /project/
---

<div>
    {% for item in site.data.project %}
    <div class="project-card">
        <h2>{{ item.name }}</h2>
        <p>
            <div><b>Backend:</b> {{ item.be-technology }} </div>
            <div><b>Frontend:</b> {{ item.fe-technology }} </div>
            <div><b>Others:</b> {{ item.other-technology }} </div>
        </p>

        <p> {{ item.description }} </p>

        <div class="project-links">
            <a href="{{ item.demo }}"> Demo </a>
            <a href="https://github.com/{{ site.github_username }}/{{ item.repository }}"> 
                <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg>
                <span>Repository</span>
            </a>
            <a href="{{ item.documentation }} "> Documentation</a>
        </div>
    </div>
    {% endfor %}
</div>