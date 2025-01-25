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
    <a href="{{ item.url }}" target="_blank">Share</a>
    {{item.content}}
</details>

{% endfor %}
