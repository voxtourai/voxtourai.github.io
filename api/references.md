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
    {{item.content}}
</details>

{% endfor %}

<details>
<summary>/updateTourTemplateImage</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/updateTourTemplateImage</div>
</details>
<details>
<summary>/getTourTemplate</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/getTourTemplate</div>
</details>
<details>
<summary>/createTour</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/createTour</div>
</details>
<details>
<summary>/getTour</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/getTour</div>
</details>
<details>
<summary>/getLocation</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/getLocation</div>
</details>