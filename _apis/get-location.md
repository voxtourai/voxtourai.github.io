---
layout: api
title: "getLocation"
order: 8
---

<div>getLocation API retrieves detailed information about a specific location, including its name, description, audio narration, and images. This API is useful for accessing location-based storytelling content for tours.</div>

<h3>Key Features</h3>
<ol>
<li>Retrieve detailed information about a location</li>
<li>Access audio narration and images related to the location</li>
<li>Integrate location-based storytelling into applications</li>
</ol>

<h3>Example Request</h3>
<div>Querying for a specific location by ID:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "locationId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b"
}
{% endhighlight %}

<h3>Request Body</h3>

<div class="request-vars">
    <span class="request-var-name">apiKey</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    A unique authentication key required for API access. This key must be included in every request to authorize and validate usage.
</div>

<div class="request-vars">
    <span class="request-var-name">locationId</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The unique identifier of the location whose details are being requested.
</div>

<h3>Example Response</h3>
Returns detailed information about the requested location, including name, description, audio, and images.

{% highlight json %}
{
    "locationId": "6e72952b-e987-4b5c-9f05-b568d622bdbf",
    "name": "Cultural Tapestry Trail: A Journey Through Toronto's Heritage",
    "text": "Union Station, a major railway station ...",
    "audio": "https://bff.voxtour.ai/downloadFile/6bb7430a-b436-4333-bb2b-690d17380254",
    "imageList": [
        {
        "imageUrl": "https://upload.wikimedia.org/wikipedia/CN_Tower.jpg",
        "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower.jpg",
        "attributionHtml": "Giorgio Galeotti, CC BY 4.0"
        },
        {
        "imageUrl": "https://upload.wikimedia.org/wikipedia/CN_Tower_Toronto.jpg",
        "sourceUrl": "https://commons.wikimedia.org/wiki/File:CN_Tower_Toronto.jpg",
        "attributionHtml": "Ken Lund, CC BY-SA 2.0"
        }
    ]
}
{% endhighlight %}

