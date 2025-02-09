---
layout: api
title: "updateTourTemplateImage"
order: 4
---

<div>updateTourTemplateImage API allows users to update the image associated with a tour template by providing a valid tour template ID and an uploaded image file ID. This API ensures that the tour template displays the latest visual representation.</div>

<h3>Key Features</h3>
<ol>
<li>Update the image of an existing tour template</li>
<li>Requires a valid <code>tourTemplateId</code> and <code>fileId</code></li>
<li>API key authentication required</li>
</ol>

<h3>Example Request</h3>
<div>Updating the image for a specific tour template:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "tourTemplateId": "6e72952b-e987-4b5c-9f05-b568d622bdbf",
   "fileId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b"
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
    <span class="request-var-name">tourTemplateId</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">The unique identifier of the tour template whose image is being updated.</div>

<div class="request-vars">
    <span class="request-var-name">fileId</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">The unique identifier of the uploaded image file to be associated with the tour template.</div>

<h3>Example Response</h3>
Returns a status code indicating a successful update:
{% highlight json %}
200
{% endhighlight %}
