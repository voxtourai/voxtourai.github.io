---
layout: default
title: General Information
parent: Help Center
description: General Information
nav_order: 1
---

# General Information

<details>
    <summary><strong>What is Document360?</strong></summary>
    <p>A well-structured product to create a world-class knowledge base for your customers and employees. Content producers get the power, whereas content consumers get the simplicity.</p>
    <h4>Core parts</h4>
    <ul>
        <li>Knowledge base portal</li>
        <li>Knowledge base site</li>
        <li>Knowledge base widget</li>
        <li>API documentation</li>
    </ul>
</details>

{% assign sorted_items = site.general_information | sort: 'order' %}
{% for item in sorted_items %}

- [{{ item.title }}]({{ item.url }})
  {% endfor %}
