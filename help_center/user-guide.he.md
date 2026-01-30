---
layout: default
title: מדריך למשתמש
parent: מרכז העזרה
description: "מדריך שלב אחר שלב לשימוש ב-VoxTour.ai: מחקירת ערים ומציאת סיורים ועד התחברות והאזנה לסיפורי אודיו, עם הסברים ברורים על התכונות והמצבים המרכזיים."
nav_order: 2
lang: he
permalink: /help_center/user-guide.html
---

# מדריך למשתמש

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
