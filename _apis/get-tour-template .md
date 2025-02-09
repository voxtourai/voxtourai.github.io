---
layout: api
title: "getTourTemplate"
order: 5
---

<div>getTourTemplate API allows users to retrieve details about a specific tour template, including its name, description, duration, and associated Points of Interest (POIs).</div>

<h3>Key Features</h3>
<ol>
<li>Retrieve a tour template by its unique ID</li>
<li>Access detailed information, including description, duration, and distance</li>
<li>Get a list of associated POIs</li>
</ol>

<h3>Example Request</h3>
<div>Retrieving details for a specific tour template:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "tourTemplateId": "6e72952b-e987-4b5c-9f05-b568d622bdbf"
}
{% endhighlight %}

<h3>Request Body</h3>
<div class="request-vars">
    <span class="request-var-name">apiKey</span>
    <span class="request-var-type">string</span>
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">A unique authentication key required for API access. Obtain your API key from the Developer Portal.</div>

<div class="request-vars">
    <span class="request-var-name">tourTemplateId</span>
    <span class="request-var-type">string</span>
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">The unique identifier of the tour template to retrieve.</div>

<h3>Example Response</h3>
Returns details of the requested tour template:
{% highlight json %}
{
    "tourTemplateId": "6e72952b-e987-4b5c-9f05-b568d622bdbf",
    "name": "Cultural Tapestry Trail: A Journey Through Toronto's Heritage",
    "description": "Embark on a cultural journey through Toronto, visiting landmarks such as CN Tower, Union Station, and more.",
    "lang": "en",
    "durationInMinutes": 240,
    "distanceInMeters": 4500,
    "poiIdList": [
        { "poiId": "edea824b-5aad-4691-98e1-1493269521b2" },
        { "poiId": "6dcfc4f0-81c5-4f19-b3df-09464a84213b" },
        { "poiId": "c5e38d48-74c4-438d-8860-d9953afab1fd" }
    ]
}
{% endhighlight %}
