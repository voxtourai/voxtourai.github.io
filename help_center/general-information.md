---
layout: default
title: General Information
parent: Help Center
description: General Information
nav_order: 1
---

# General Information

{% assign sorted_items = site.general_information | sort: 'order' %}
{% for item in sorted_items %}

    <details>
        <summary><b>{{ item.title }}</b></summary>
        {{item.content}}
        <a href="{{ item.url }}">Share</a>
    </details>

{% endfor %}
