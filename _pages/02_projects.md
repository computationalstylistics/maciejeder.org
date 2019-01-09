---
layout: page
title: projects
permalink: /projects/
description: A selection of the projects that I’ve been conducting recently or which I consider anyway important.
ref: projects
lang: en
---


{% assign subset=site.projects | where:"lang", page.lang %}
{% for project in subset %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.thumbnail | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div>
    <div class="profile col one right">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        <img class="one" src="{{ project.thumbnail | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}"></a>
    </div>
    <div><a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        <h2>{{ project.title }}</h2></a>
        <span>{{ project.description }}</span>
<!--        <span> (<a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">more...</a>).</span> -->
    </div>
    <hr/>
</div>


{% endif %}

{% endfor %}
