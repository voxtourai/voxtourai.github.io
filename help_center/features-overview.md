---
layout: default
title: Features Overview
parent: Help Center
description: "Overview of VoxTour.ai features like VoxExplore, VoxRoute, and VoxLens, with quick guidance for each mode."
nav_order: 2
permalink: /help_center/features-overview.html
---

# Features Overview

{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.features_overview | sort: 'order' %}
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
