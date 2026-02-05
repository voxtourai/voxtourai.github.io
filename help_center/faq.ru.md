---
layout: default
title: FAQ
parent: Центр помощи
description: "Раздел FAQ помогает быстро найти ответы на самые распространённые вопросы о VoxTour.ai. Здесь вы найдёте краткие и понятные объяснения по запуску туров, использованию умных инструментов Navigator и Frame, управлению аккаунтом и решению технических проблем. Если вам нужны подробные инструкции, ответы FAQ содержат ссылки на полные статьи Руководства пользователя."
nav_order: 4
permalink: /help_center/faq.html
lang: ru
---

# Часто задаваемые вопросы

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
    <a href="{{ item.url }}"><img alt="Поделиться" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
