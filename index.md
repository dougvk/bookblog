---
layout: page
title: Transcending Binaries
---
{% include JB/setup %}

{% for post in site.posts limit:5 %}
<h1 class="h2 entry-title"><a href="{{ post.url }}">{{ post.title }}</a></h1>
{{ post.content | truncatehtml: 1000 }}
<div class="meta">
    <p class="date-publish">
        <a href="{{ post.url }}">Read More &amp; Comment...</a>
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
-----
{% endfor %}
