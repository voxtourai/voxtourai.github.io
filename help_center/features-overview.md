---
layout: default
title: Features Overview
parent: Help Center
description: Features Overview
nav_order: 2
---

# Features Overview

{% assign sorted_items = site.features_overview | sort: 'order' %}
{% for item in sorted_items %}

<details>
    <summary>{{ item.title }}</summary>
    {{item.content}}
    <a href="{{ item.url }}"><img alt="Share" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
