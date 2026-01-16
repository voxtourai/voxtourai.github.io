---
layout: default
title: Общая информация
parent: Центр помощи
description: Общая информация
nav_order: 1
lang: ru
permalink: /help_center/general-information.html
---

# Общая информация

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
