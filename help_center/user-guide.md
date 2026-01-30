---
layout: default
title: User Guide
parent: Help Center
description: "Step-by-step guide to using VoxTour.ai, from exploring cities and finding tours to signing in and listening to audio stories, with clear explanations of key features and modes."
nav_order: 2
permalink: /help_center/user-guide.html
---

# User Guide

{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.user_guide | sort: 'order' %}
{% if active_lang == site.default_lang %}
{% assign filtered_items = sorted_items | where_exp: "item", "item.lang == nil or item.lang == active_lang" %}
{% else %}
{% assign filtered_items = sorted_items | where: "lang", active_lang %}
{% endif %}
{% for item in filtered_items %}

<details>
    <summary>{{ item.title }}</summary>
    {{item.content}}
    <a href="{{ item.url }}"><img alt="Share" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
