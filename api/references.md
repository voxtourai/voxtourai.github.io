---
layout: default
title: API References
parent: API
description: VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
---

# API References

VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
<details>
<summary>Search POIs by different criteria</summary>
<div class="api-url-box">POST https://api.voxtour.ai/v1/queryPOIs</div>
<div>The POI Query API allows users to search for Points of Interest (POIs) within a specified geographical area based on keywords, categories, or ranking criteria. The API returns a structured list of POIs with details such as name, description, location, images, and metadata.</div>
<b>Key Features</b>
<ol>
<li>Search POIs by different criteria (e.g., keyword, location, language)</li>
<li>Filter results using a bounding box (latitude/longitude)</li>
<li>Sort results by relevance or custom criteria</li>
<li>Retrieve detailed POI information, including descriptions, images, and external links</li>
</ol>
<b>Example Request</b>
<div>Querying for POIs named "Tower" within a defined bounding box:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "lang": "en",
   "search": "Tower",
   "boundingBox": [
       43.300000,
       44.100000,
       -80.000000,
       -78.500000
   ],
   "firstSortBy": null,
   "firstSortDescending": false,
   "secondSortBy": null,
   "secondSortDescending": false,
   "pageSize": 200,
   "pageNumber": 1
}
{% endhighlight %}
</details>
<details>
<summary>Create Tour Route.</summary>

The POI Query API allows users to search for Points of Interest (POIs) within a specified geographical area based on keywords, categories, or ranking criteria. The API returns a structured list of POIs with details such as name, description, location, images, and metadata.

*Key Features*
1. Search POIs by different criteria (e.g., keyword, location, language).
2. Filter results using a bounding box (latitude/longitude).
3. Sort results by relevance or custom criteria.
4. Retrieve detailed POI information, including descriptions, images, and external links

*Example Request*
</details>