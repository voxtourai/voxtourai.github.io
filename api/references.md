---
layout: default
title: API References
parent: API
description: VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
---

# API References

VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
<details>
<summary>/queryPOIs</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/queryPOIs</div>
<div>The POI Query API allows users to search for Points of Interest (POIs) within a specified geographical area based on keywords, categories, or ranking criteria. The API returns a structured list of POIs with details such as name, description, location, images, and metadata.</div>
<h3>Key Features</h3>
<ol>
<li>Search POIs by different criteria (e.g., keyword, location, language)</li>
<li>Filter results using a bounding box (latitude/longitude)</li>
<li>Sort results by relevance or custom criteria</li>
<li>Retrieve detailed POI information, including descriptions, images, and external links</li>
</ol>
<h3>Example Request</h3>
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
<h3>Request body</h3>
<div class="request-vars">
    <span class="request-var-name">apiKey</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">A unique authentication key required for API access. This key must be included in every request to authorize and validate usage. Obtain your API key from the VoxTour.ai Developer Portal.</div>
<div class="request-vars">
    <span class="request-var-name">lang</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-optional">Optional</span>
    <span class="request-var-defaults">Defaults to en</span>
</div>
<div class="request-vars-description">
    Specifies the language for the response content. Uses ISO 639-1 codes (e.g., "en" for English, "fr" for French). If not provided, the default language is English.
</div>
<div class="request-vars">
    <span class="request-var-name">search</span> 
    <span class="request-var-type">string or null</span> 
    <span class="request-var-optional">Optional</span>
    <span class="request-var-defaults">Defaults to false</span>
</div>
<div class="request-vars-description">
    A keyword or phrase used to filter Points of Interest (POIs) by name or related terms. If omitted, the API returns all POIs within the specified bounding box.
</div>
<div class="request-vars">
    <span class="request-var-name">boundingBox</span> 
    <span class="request-var-type">array</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    Defines the geographical area for the POI search. The array must contain four numerical values representing the southwest latitude, northeast latitude, southwest longitude, and northeast longitude. POIs within this bounding box will be included in the response.
    <br><strong>Example:</strong> <code>[43.300000, 44.100000, -80.000000, -78.500000]</code>
</div>

<h3>Example Response</h3>
Returns a list of matching POIs, including name, description, coordinates, and images:
{% highlight json %}
{
   "poiList": [
       {
           "poiId": "87a1478a-7363-4dc4-818a-141eff446880",
           "name": "CN Tower",
           "info": "The CN Tower detailed description.",
           "nativeName": "CN Tower",
           "category": "ArchitecturalMarvel",
           "subcategory": "Skyscraper",
           "address": "CN Tower, 290, Bremner Boulevard, Toronto, Ontario, M5V 3L9, Canada",
           "latitude": 43.6425637,
           "longitude": -79.38708718320467,
           "imageList": [
               {
                   "imageUrl": "https://upload.wikimedia.org/wikipedia/commons/thumb/CN_Tower_1.jpg",
                   "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower_1.jpg",
                   "attributionHtml": "Giorgio Galeotti,CC BY 4.0, via Wikimedia Commons"
               },
               {
                   "imageUrl": "https://upload.wikimedia.org/wikipedia/commons/thumb/CN_Tower_2.jpg",
                   "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower_2.jpg",
                   "attributionHtml": "Ken Lund, CC BY-SA 2.0, via Wikimedia Commons"
               }
           ],
           "hashtagMap": {},
           "metadata": [
               {
                   "name": "wikipedia",
                   "value": "en:CN Tower",
                   "timestamp": "2024-06-03T12:17:00.568101Z"
               },
               {
                   "name": "website",
                   "value": "https://www.cntower.ca/",
                   "timestamp": "2024-05-26T02:48:45.475446Z"
               }
           ],
           "rank": 0.8958864102649058
       }
   ]
}
{% endhighlight %}
</details>
<details>
<summary>/createTourTemplate</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/createTourTemplate</div>
<div>The Create Tour Template API allows users to generate a custom tour template by defining a name, description, language, duration, distance, and a list of Points of Interest (POIs). The API returns a unique <code>tourTemplateId</code> for managing or modifying the template later.</div>
<h3>Key Features</h3>
<ol>
    <li>Create a tour template with a custom name and description</li>
    <li>Define tour duration and total distance</li>
    <li>Include multiple POIs to structure an itinerary</li>
    <li>Retrieve a unique <code>tourTemplateId</code> for future modifications</li>
</ol>

<h3>Example Request</h3>
<div>Creating a cultural tour template in Toronto:</div>
{% highlight json %}
{
  "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
  "name": "Cultural Tapestry Trail: A Journey Through Toronto's Heritage",
  "description": "Embark on a cultural journey along Toronto’s most iconic landmarks...",
  "lang": "en",
  "durationInMinutes": 240,
  "distanceInMeters": 4500,
  "poiIdList": [
      { "poiId": "edea824b-5aad-4691-98e1-1493269521b2" },
      { "poiId": "6dcfc4f0-81c5-4f19-b3df-09464a84213b" }
  ]
}
{% endhighlight %}

<h3>Request Body</h3>
<div class="request-vars">
    <span class="request-var-name">apiKey</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    A unique authentication key required for API access. This key must be included in every request to authorize and validate usage. Obtain your API key from the VoxTour.ai Developer Portal.
</div>

<div class="request-vars">
    <span class="request-var-name">name</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The name of the tour template. This should be a descriptive title that reflects the theme or focus of the tour.
</div>

<div class="request-vars">
    <span class="request-var-name">description</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Optional</span>
</div>
<div class="request-vars-description">
    A detailed description of the tour, outlining its purpose, key highlights, and points of interest.
</div>

<div class="request-vars">
    <span class="request-var-name">lang</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-optional">Optional</span>
    <span class="request-var-defaults">Defaults to "en"</span>
</div>
<div class="request-vars-description">
    Specifies the language for the tour template. Uses ISO 639-1 codes (e.g., "en" for English, "fr" for French).
</div>

<div class="request-vars">
    <span class="request-var-name">durationInMinutes</span> 
    <span class="request-var-type">integer</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The estimated duration of the tour in minutes.
</div>

<div class="request-vars">
    <span class="request-var-name">distanceInMeters</span> 
    <span class="request-var-type">integer</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The total distance covered by the tour in meters.
</div>

<div class="request-vars">
    <span class="request-var-name">poiIdList</span> 
    <span class="request-var-type">array</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    A list of Points of Interest (POIs) included in the tour. Each POI is identified by a unique <code>poiId</code>.
</div>

<h3>Example Response</h3>
Returns a unique <code>tourTemplateId</code> for future modifications or retrieval:
{% highlight json %}
{
"tourTemplateId": "5c744b2b-8f6c-4be1-baf0-409e43a4e06e"
}
{% endhighlight %}
</details>
<details>
<summary>/uploadImage</summary>
<div class="api-url-box"><span>POST</span> https://api.voxtour.ai/v1/uploadImage</div>
</details>
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