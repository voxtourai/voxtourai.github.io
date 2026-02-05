---
layout: default
title: FAQ
parent: Help Center
description: "La sección FAQ te ayuda a encontrar rápidamente respuestas a las preguntas más comunes sobre VoxTour.ai. Ya sea que necesites ayuda para iniciar un tour, usar herramientas inteligentes como Navigator o Frame, administrar tu cuenta o resolver problemas técnicos, aquí encontrarás explicaciones claras y breves. Si necesitas instrucciones detalladas, las respuestas del FAQ incluyen enlaces a artículos completos de la Guía del Usuario."
nav_order: 4
permalink: /help_center/faq.html
lang: es
---

# Preguntas Frecuentes

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
    <a href="{{ item.url }}"><img alt="Compartir" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
