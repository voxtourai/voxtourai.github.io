---
layout: default
title: "uploadImage"
order: 3
---
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
