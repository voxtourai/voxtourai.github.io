---
layout: api
title: "getTour"
order: 7
---

<div>getTour API allows users to retrieve detailed information about a specific tour using its unique identifier. The response includes the tour's template ID and a list of locations featured in the tour, each with a unique location ID and name.</div>

<h3>Key Features</h3>
<ol>
<li>Retrieve detailed information about a tour using its unique ID</li>
<li>Get a list of locations included in the tour</li>
<li>Each location contains a unique ID and name</li>
</ol>

<h3>Example Request</h3>
<div>Fetching details for a specific tour using its ID:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "tourId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b"
}
{% endhighlight %}

<h3>Request Body</h3>
<div class="request-vars">
    <span class="request-var-name">apiKey</span>
    <span class="request-var-type">string</span>
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">A unique authentication key required for API access. This key must be included in every request to authorize and validate usage.</div>

<div class="request-vars">
    <span class="request-var-name">tourId</span>
    <span class="request-var-type">string</span>
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">The unique identifier of the tour for which details are requested.</div>

<h3>Example Response</h3>
Returns details of the requested tour, including its template ID and a list of locations:
{% highlight json %}
{
    "tourId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b",
    "tourTemplateId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b",
    "locationList": [
        {
            "locationId": "edea824b-5aad-4691-98e1-1493269521b2",
            "name": "Toronto City Hall"
        },
        {
            "locationId": "6dcfc4f0-81c5-4f19-b3df-09464a84213b",
            "name": "Eaton Centre"
        },
        {
            "locationId": "c5e38d48-74c4-438d-8860-d9953afab1fd",
            "name": "Yonge-Dundas Square"
        },
        {
        "locationId": "4b013a3e-60a6-4b99-97b9-5e46c6d0582a",
            "name": "St. Lawrence Market"
        },
        {
            "locationId": "5c744b2b-8f6c-4be1-baf0-409e43a4e06e",
            "name": "Union Station"
        },
        {
            "locationId": "59433eec-63e1-4aef-9322-a077b78f3cd8",
            "name": "CN Tower"
        }
    ]
}
{% endhighlight %}

