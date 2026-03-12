---
layout: default
title: VoxTour Integration
parent: API & Widgets
description: Integrate VoxTour audio guides into websites, applications, and digital platforms.
---

# VoxTour Integration

VoxTour integrations allow developers, partners, and content platforms to embed interactive audio guides directly into their websites, applications, and digital experiences.

Using VoxTour’s widgets, APIs, and platform tools, you can easily add immersive audio tours to travel websites, tourism portals, blogs, mobile apps, and other digital products.

VoxTour integrations are designed to be simple to implement while remaining flexible for a wide range of use cases — from embedding a single audio guide on a blog post to powering large-scale travel platforms.

{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.faq | sort: 'order' %}
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