---
layout: default
title: Integración de VoxTour
parent: API & Widgets
description: Integre guías de audio de VoxTour en sitios web, aplicaciones y plataformas digitales.
lang: es
---

# Integración de VoxTour

Las integraciones de VoxTour permiten a desarrolladores, socios y plataformas de contenido incrustar guías de audio interactivas directamente en sus sitios web, aplicaciones y experiencias digitales.

Utilizando los widgets, APIs y herramientas de la plataforma VoxTour, puede añadir fácilmente recorridos de audio inmersivos a sitios web de viajes, portales de turismo, blogs, aplicaciones móviles y otros productos digitales.

Las integraciones de VoxTour están diseñadas para ser fáciles de implementar, manteniendo al mismo tiempo la flexibilidad necesaria para una amplia variedad de casos de uso, desde incrustar una sola guía de audio en una publicación de blog hasta impulsar plataformas de viajes a gran escala.

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
