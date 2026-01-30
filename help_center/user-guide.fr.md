---
layout: default
title: Guide d’utilisation
parent: Centre d'aide
description: "Guide étape par étape pour utiliser VoxTour.ai : de l’exploration des villes et la recherche de visites à la connexion et l’écoute d’histoires audio, avec des explications claires des fonctionnalités et des modes clés."
nav_order: 2
lang: fr
permalink: /help_center/user-guide.html
---

# Guide d’utilisation

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
