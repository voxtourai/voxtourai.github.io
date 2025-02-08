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
    <summary>{{ item.title }}</summary>
    {{item.content}}
</details>

{% endfor %}

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
  "description": "Embark on a cultural journey along Toronto’s most iconic landmarks",
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
    <span class="request-var-optional">Optional</span>
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
<div>The Upload Image API allows users to upload an image file and receive a unique image ID in response. This API supports multipart form data and requires an API key for authentication.</div>

<h3>Key Features</h3>
<ol>
<li>Upload image files using multipart form data</li>
<li>Receive a unique image ID for reference</li>
<li>Requires an API key for authentication</li>
</ol>

<h3>Example Request</h3>
<div>Uploading an image file:</div>

{% highlight http %}
POST /uploadImage
Headers:
Content-Type: multipart/form-data
{% endhighlight %}

<h3>Request Body (Form-Data)</h3>

<div class="request-vars">
    <span class="request-var-name">apiKey</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">A unique authentication key required for API access. This key must be included in every request to authorize and validate usage. Obtain your API key from the VoxTour.ai Developer Portal.</div>

<div class="request-vars">
    <span class="request-var-name">file</span> 
    <span class="request-var-type">file</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The image file to be uploaded. Supported formats: JPG, PNG, and GIF.
</div>

<h3>Example Response</h3>
Returns a unique file ID:

{% highlight json %}
{
"fileId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b"
}
{% endhighlight %}

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