---
layout: default
title: סקירת תכונות
parent: מרכז עזרה
description: "סקירה של פיצ'רים ב-VoxTour.ai כמו VoxExplore, VoxRoute ו-VoxLens, עם הנחיה קצרה לשימוש בכל מצב."
nav_order: 3
lang: he
permalink: /help_center/features-overview.html
---

# סקירת תכונות

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
