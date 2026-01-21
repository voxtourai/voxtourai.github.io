---
layout: default
title: מידע כללי
parent: מרכז עזרה
description: "מידע כללי על VoxTour.ai: מה זה, איך מתחילים, מכשירים נתמכים, חיבור לאינטרנט, יצירת תוכן וטקסט-לדיבור."
nav_order: 1
lang: he
permalink: /help_center/general-information.html
---

# מידע כללי

{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.general_information | sort: 'order' %}
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
