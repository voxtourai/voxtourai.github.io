---
layout: default
title: Integrazione VoxTour
parent: API & Widgets
description: Integra le audioguide VoxTour in siti web, applicazioni e piattaforme digitali.
lang: it
---

# Integrazione VoxTour

Le integrazioni VoxTour permettono a sviluppatori, partner e piattaforme di contenuti di incorporare audioguide interattive direttamente nei loro siti web, applicazioni ed esperienze digitali.

Utilizzando i widget, le API e gli strumenti della piattaforma VoxTour, è possibile aggiungere facilmente tour audio immersivi a siti web di viaggio, portali turistici, blog, applicazioni mobili e altri prodotti digitali.

Le integrazioni VoxTour sono progettate per essere semplici da implementare pur rimanendo flessibili per una vasta gamma di casi d’uso, dall’inserimento di una singola audioguida in un articolo di blog fino all’alimentazione di grandi piattaforme di viaggio.

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