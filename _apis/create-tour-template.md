---
layout: default
title: "createTourTemplate"
order: 2
---

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