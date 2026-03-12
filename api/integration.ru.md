---
layout: default
title: Интеграция VoxTour
parent: API & Widgets
description: Интеграция аудиогидов VoxTour в сайты, приложения и цифровые платформы.
lang: ru
---

# Интеграция VoxTour

Интеграции VoxTour позволяют разработчикам, партнёрам и контент-платформам встраивать интерактивные аудиогиды непосредственно в свои сайты, приложения и цифровые сервисы.

Используя виджеты, API и инструменты платформы VoxTour, вы можете легко добавить иммерсивные аудиотуры на туристические сайты, туристические порталы, блоги, мобильные приложения и другие цифровые продукты.

Интеграции VoxTour разработаны так, чтобы их было легко внедрять, сохраняя при этом гибкость для широкого спектра сценариев использования — от встраивания одного аудиогида в блог-пост до поддержки крупных туристических платформ.
{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.integration | sort: 'order' %}
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