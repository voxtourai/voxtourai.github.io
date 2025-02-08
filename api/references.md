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