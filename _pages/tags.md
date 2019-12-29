---
layout: page
title: Tagi
permalink: /tags/
description: Tagi artykułów
---
<div class="posts">
    <ul class="posts-nav">
        {% assign tags = site.tags | sort: "title" %}
        {% for node in tags %}
        {% if node.title != null and node.layout == "page_tag" %}
        <li>
            <a class="posts-nav-item" href="{{ node.url | relative_url }}">{{ node.title }}</a>
        </li>
        {% endif %}
        {% endfor %}
    </ul>
</div>