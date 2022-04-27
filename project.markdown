---
layout: project
title: Projects
permalink: /project/
---

<div>
    {% for item in site.data.project %}
    <div class="project-card">

        <div class="project-heading">
            <span class="project-title">{{item.projectName}}</span>
        </div>

        <span>{{item.projectDescription}}</span>
        <a href="https://{{ site.atlassian_username }}.atlassian.net/{{ item.documentation }}"> 
            <img class="img-icon" src="/assets/atlassian-icon.png"/>
            <span>Open confluence documentation</span>
        </a>

        <div class="project-demo">
            <img src="https://speedkt-portfolio.s3.amazonaws.com/speedkt-people-microservice.jpg"/>
        </div>

        <div class="project-module-container">
            {% for module in item.modules %}
                <div class="project-module-card">
                    <div>{{ module.moduleName }}</div>
                    <span> {{ module.properties.description }} </span>
                    
                    <div class="project-module-properties">
                        <div><b>Tech stack:</b> {{ module.properties.techstack }} </div>
                    </div>

                    <a class="project-module-repo" href="https://github.com/{{ site.github_username }}/{{ module.properties.repository }}"> 
                        <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg>
                        <span>Repository</span>
                    </a>
                </div>
            {% endfor %}
        </div>

    </div>
    {% endfor %}
</div>