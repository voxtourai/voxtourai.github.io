---
layout: default
title: Informazioni generali
parent: Centro assistenza
description: "Informazioni generali su VoxTour.ai: cos’è, come iniziare, dispositivi supportati, connessione internet, creazione dei contenuti e sintesi vocale."
nav_order: 1
lang: it
permalink: /help_center/general-information.html
---

# Informazioni generali

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
