---
layout: default
title: Guía de usuario
parent: Centro de ayuda
description: "Guía paso a paso para usar VoxTour.ai: desde explorar ciudades y encontrar tours hasta iniciar sesión y escuchar historias en audio, con explicaciones claras de las funciones y modos clave."
nav_order: 2
lang: es
permalink: /help_center/user-guide.html
---

# Guía de usuario

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
