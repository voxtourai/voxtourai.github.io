---
layout: default
title: Guida all’uso
parent: Centro assistenza
description: "Guida passo dopo passo all’utilizzo di VoxTour.ai: dall’esplorazione delle città e la ricerca dei tour all’accesso e all’ascolto di storie audio, con spiegazioni chiare delle funzionalità e delle modalità principali."
nav_order: 2
lang: it
permalink: /help_center/user-guide.html
---

# Guida all’uso


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
