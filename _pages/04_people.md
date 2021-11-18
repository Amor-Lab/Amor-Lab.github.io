---
layout: page
title: People
permalink: /people/
---

<style>
    .row{
        display: flex;
    }

</style>

{% for member in site.data.lab_members.members %}
<div class="row align-items-center">
    <div class="col-lg-4">
        <div class="row justify-content-center">
            {{ member.title }}
        </div>
            <img class="img-responsive" src="../img/{{ member.image }}" style="width:100%"/>
        <div class="row justify-content-center">
            {{ member.name }}
        </div>
        <div class="row justify-content-center">
            <a href="mailto:{{ member.mail }}" target="_blank"> {{ member.mail }} </a>
        </div>
        <div class="row justify-content-center">
            {% if member.twitter %}
            <a href="https://twitter.com/{{ member.twitter }}" target="_blank"><i class="fab fa-twitter"></i></a>
            {% endif %}
            {% if member.linkedin %}
            <a href="https://www.linkedin.com/in/{{ member.linkedin }}" target="_blank"><i class="fab fa-linkedin"></i></a>
            {% endif %}
        </div>
    </div>
    <div class="col-lg-8">
        {{ member.summary }}
    </div>
</div>
{% endfor %}

