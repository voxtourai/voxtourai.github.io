---
layout: default
title: FAQ
parent: Centro assistenza
description: "La sezione FAQ ti aiuta a trovare rapidamente risposte alle domande più comuni su VoxTour.ai. Che tu abbia bisogno di aiuto per iniziare un tour, utilizzare strumenti intelligenti come Navigator o Frame, gestire il tuo account o risolvere problemi tecnici, qui troverai spiegazioni brevi e chiare. Se hai bisogno di istruzioni dettagliate, le risposte FAQ includono link agli articoli completi della Guida Utente."
nav_order: 4
permalink: /help_center/faq.html
lang: it
---

# Domande Frequenti

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
    <a href="{{ item.url }}"><img alt="Condividi" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
