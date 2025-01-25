---
layout: default
title: General Information
parent: Help Center
description: General Information
nav_order: 1
---

# General Informationz

{% assign sorted_items = site.general_information | sort: 'order' %}
{% for item in sorted_items %}

{% if item.renderFile %}
{% include_relative item.renderFile %}
{% endif %}

- [{{ item.title }}]({{ item.url }})
  {% endfor %}
