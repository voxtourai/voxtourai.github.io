---
layout: default
title: FAQ
parent: Help Center
description: "The FAQ section helps you quickly find answers to the most common questions about VoxTour.ai. Whether you need help starting a tour, using Smart Tools like Navigator or Frame, managing your account, or solving technical issues, you can find short, clear explanations here. If you need detailed instructions, FAQ answers include links to full User Guide articles."
nav_order: 4
permalink: /help_center/faq.html
---

# Frequently Asked Questions

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
    <a href="{{ item.url }}"><img alt="Share" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}
