---
layout: api
title: "createTour"
order: 6
---

<div>createTour API allows users to generate a customized tour from an existing template. Users can define storytelling preferences, select a voice assistant, and tailor the experience based on audience demographics and thematic focus.</div>

<h3>Key Features</h3>
<ol>
<li>Create a personalized tour using a predefined template</li>
<li>Customize storytelling style with adjustable parameters</li>
<li>Choose a voice assistant for narration</li>
<li>Define a unique tour theme and focus</li>
</ol>

<h3>Example Request</h3>
<div>Creating a tour with custom storytelling settings:</div>
{% highlight json %}
{
   "apiKey": "12345678-90ab-cdef-1234-567890abcdef",
   "tourTemplateId": "6e72952b-e987-4b5c-9f05-b568d622bdbf",
   "voiceAssistant": "William",
   "averageAge": 40,
   "storytellingControls": {
       "Formality": 4,
       "ToneOfVoice": 4,
       "ComplexityLevel": 3,
       "EmpathyLevel": 1,
       "ImaginationLevel": 1,
       "DetailLevel": 4,
       "CulturalSensitivity": 1,
       "OptimismPessimism": 3,
       "LanguageStyle": 3
   },
   "tourTheme": "This tour focuses on Modern Toronto, showcasing the ..."
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
    <span class="request-var-name">tourTemplateId</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-required">Required</span>
</div>
<div class="request-vars-description">
    The unique identifier of the tour template from which the new tour will be created.
</div>

<div class="request-vars">
    <span class="request-var-name">voiceAssistant</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-optional">Optional</span>
</div>
<div class="request-vars-description">
    The name of the voice assistant that will narrate the tour.
</div>

<div class="request-vars">
    <span class="request-var-name">averageAge</span> 
    <span class="request-var-type">integer</span> 
    <span class="request-var-optional">Optional</span>
</div>
<div class="request-vars-description">
    The estimated average age of the tour audience, influencing storytelling complexity.
</div>

<div class="request-vars">
    <span class="request-var-name">storytellingControls</span> 
    <span class="request-var-type">object</span> 
    <span class="request-var-optional">Optional</span>
</div>
<div class="request-vars-description">
    A set of parameters controlling the storytelling style, including formality, tone of voice, complexity level, and cultural sensitivity.
</div>

<div class="request-vars">
    <span class="request-var-name">tourTheme</span> 
    <span class="request-var-type">string</span> 
    <span class="request-var-optional">Optional</span>
</div>
<div class="request-vars-description">
    A brief description of the tour's theme, such as historical, cultural, or modern architecture.
</div>

<h3>Example Response</h3>
Returns a unique identifier for the newly created tour:

{% highlight json %}
{
    "tourId": "a7b1ac9d-3f64-4bd5-ad84-5cf59a72045b"
}
{% endhighlight %}

