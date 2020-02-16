---
layout: page
title: projekty
permalink: /pl/projekty/
description: Wybrane projekty, którymi się zajmowałem niedawno lub które z różnych powodów uważam za istotne.
ref: projects
lang: pl
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
<!--        <span> (<a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">więcej...</a>).</span> -->
    </div>
<hr/>
</div>




{% endif %}

{% endfor %}
