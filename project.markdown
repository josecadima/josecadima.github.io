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
            <div><b>Other:</b> {{ item.other-technology }} </div>
            <div><b>Tools:</b> {{ item.tool }} </div>
        </p>

        <p> {{ item.description }} </p>

        <div class="project-links">
            <a href="{{ item.demo }}">
                <img class="img-icon" src="/assets/play-icon.png"/>
                <span>Demo</span>
            </a>
            
            <a href="https://github.com/{{ site.github_username }}/{{ item.repositoryApi }}"> 
                <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg>
                <span>API repo</span>
            </a>

            <a href="https://github.com/{{ site.github_username }}/{{ item.repositoryWeb }}"> 
                <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg>
                <span>WEB repo</span>
            </a>

            <a href="https://{{ site.atlassian_username }}.atlassian.net/{{ item.documentation }}"> 
                <img class="img-icon" src="/assets/atlassian-icon.png"/>
                <span>Documentation</span>
            </a>
        </div>
    </div>
    {% endfor %}
</div>