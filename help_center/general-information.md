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
    <summary><span style="line-height: 3.4; color: #34aeeb; font-weight: bold;">{{ item.title }}</span></summary>
    <a href="{{ item.url }}" target="_blank">Share</a>
    {{item.content}}
</details>

{% endfor %}
