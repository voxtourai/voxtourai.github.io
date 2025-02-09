---
layout: default
title: API References
parent: API
description: VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
---

# API References

VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.

{% assign sorted_apis = site.apis | sort: 'order' %}
{% for item in sorted_apis %}

<details>
    <summary>/{{ item.title }}</summary>
    <div class="api-url-box">
        <div class="api-url">
            <span>POST</span> https://api.voxtour.ai/v1/{{ item.title }}
        </div>
        <div class="api-share">
            <a href="{{ item.url }}"><img alt="Share" src="/assets/images/share-icon-20x20.png"></a>
        </div>
    </div>
    {{item.content}}
</details>

{% endfor %}