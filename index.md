---
layout: page
title: Sup brohans
tagline: wordness
---
{% include JB/setup %}

{% for post in site.posts limit:5 %}
<div class="entry-content">
    {{ post.content | substring: 0, 100}}
    <div class="meta">
        <p class="date-publish">
            <a href="{{ post.url }}">Permalink</a>
            <span><br /><br />Published: {{ post.date | date: "%b %d, %Y" }}</span>
        </p>
        <ul class="list-category list-linear">
            <li class="list-head">category: </li>
            {% assign categories_list = post.categories %}
            {% include JB/categories_list %}
        </ul>
        <ul class="list-tag list-linear">
            <li class="list-head">tags: </li>
            {% assign tags_list = post.tags %}
            {% include JB/tags_list %}
        </ul>
    </div>
</div>
{% endfor %}
