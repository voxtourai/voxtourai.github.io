---
layout: default
title: Intégration VoxTour
parent: API & Widgets
description: Intégrez des audioguides VoxTour dans des sites web, des applications et des plateformes numériques.
lang: fr
---

# Intégration VoxTour

Les intégrations VoxTour permettent aux développeurs, partenaires et plateformes de contenu d’intégrer des audioguides interactifs directement dans leurs sites web, applications et expériences numériques.

En utilisant les widgets, API et outils de la plateforme VoxTour, vous pouvez facilement ajouter des visites audio immersives à des sites de voyage, des portails touristiques, des blogs, des applications mobiles et d’autres produits numériques.

Les intégrations VoxTour sont conçues pour être simples à mettre en œuvre tout en restant suffisamment flexibles pour un large éventail de cas d’utilisation, allant de l’intégration d’un seul audioguide dans un article de blog à l’alimentation de grandes plateformes de voyage.

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