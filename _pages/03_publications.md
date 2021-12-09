---
layout: page
title: Publications
permalink: /publications/
---

<style>
    .row{
        display: flex;
    }

</style>

<div class="post-content">
{% for year in site.data.publications.years %}
    <h1> {{ year.year.number }} </h1>
    {% for pub in year.year.publications %}
        <h4><ins><a href="{{ pub.link }}"> {{ pub.title }}</a></ins></h4>
    <p>
        {% for author in pub.authors %}
            {% if pub.lab_members contains author %}
                <strong>{{ author }}</strong>,
            {% else %}
                {{ author }},
            {% endif %}
        {% endfor %}
    </p>
    <p>
    <strong>{{ pub.journal }}</strong>. {{ pub.paper_info}}.
    </p>
    {% if pub.other %}
        <p><ins> {{ pub.other}} </ins></p>
    {% endif %}

    {% endfor %}
{% endfor %}
</div>