---
layout: default
title: FAQ
parent: Help Center
description: "La section FAQ vous aide à trouver rapidement des réponses aux questions les plus courantes sur VoxTour.ai. Que vous ayez besoin d’aide pour démarrer une visite, utiliser des outils intelligents comme Navigator ou Frame, gérer votre compte ou résoudre des problèmes techniques, vous trouverez ici des explications courtes et claires. Si vous avez besoin d’instructions détaillées, les réponses FAQ incluent des liens vers des articles complets du Guide d’utilisation."
nav_order: 4
permalink: /help_center/faq.html
lang: fr
---

# Questions Fréquemment Posées

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
    <a href="{{ item.url }}"><img alt="Partager" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
