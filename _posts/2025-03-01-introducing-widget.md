---
layout: post
title: VoxTour.ai Widget
parent: Blog
excerpt: VoxTour.ai Widget - Bringing Immersive Self-Guided Audio Tours to Any Website
author: Michael Lifshits
date: 2025-03-01
header_image: /assets/images/introducing-widget.webp
---

<style>
    html, body {
        height: 100%;
        margin: 0;
    }
    .voxtour-widget-container {
        width: 720px;
        height: 700px;
        border: 3px solid #aaa;
        border-radius: 6px;
        padding: 5px;
    }
    .voxtour-widget {
        width: 100%;
        height: 100%;
        border: none;
        pointer-events: auto;
    }
    .voxtour-full-screen {
        width: 100vw !important;
        height: 100vh !important;
        position: fixed !important;
        top: 0 !important;
        left: 0 !important;
        z-index: 9999 !important;
        border: none !important;
        border-radius: 0 !important;
        padding: 0 !important;
        background: #fff;
    }
</style>

# VoxTour.ai Widget - Bringing Immersive Self-Guided Audio Tours to Any Website

In today's digital landscape, engaging content is key to attracting and retaining visitors. Whether you run a travel blog, a tourism portal, or a local business directory, offering unique and interactive experiences can set you apart. That’s where the VoxTour Widget comes in - a powerful tool that lets you seamlessly embed audio self-guided tours directly into your website.

---

## 1. What is the VoxTour Widget?

The **VoxTour Widget** is an embeddable audio tour player that enables website owners to integrate high-quality, self-guided tours into their digital platforms. It allows visitors to listen to curated storytelling, discover nearby points of interest, and engage with locations in a way that feels both informative and immersive.

With just a few lines of code, you can add a fully functional tour experience to portals, blogs, hotel websites, event pages, and more. No additional software or technical expertise is required - just copy, paste, and let your visitors explore!

---

## Why Add the VoxTour Widget to Your Website?

### 1. Enhance Engagement with Interactive Content
People love discovering places through stories. With VoxTour, your audience can listen to professionally narrated tours, learning about destinations at their own pace. This creates a deeper connection with the content and encourages longer visits.

### 2. Increase Time Spent on Your Website
A well-placed tour can captivate users, keeping them on your site for longer periods. Whether they’re planning a trip, exploring local attractions, or diving into historical narratives, they’ll stay engaged—and more likely to explore other content you offer.

### 3. Monetization Opportunities
For travel bloggers and tourism businesses, VoxTour provides an opportunity to monetize content. By embedding tours, you can integrate premium experiences or partner with local businesses for sponsored content.

### 4. Seamless User Experience Across Devices
The widget is designed to be mobile-friendly, ensuring a smooth experience on smartphones, tablets, and desktops. Whether visitors are at home planning their next trip or on-location exploring, they can access the tour effortlessly.

### 5. Easy Integration & Customization
Adding the widget is as simple as copying and pasting an embed code into your site. Plus, the design is customizable to match your website’s aesthetic, allowing for a cohesive and professional look.

---

## Example: Amsterdam Audio Tour Widget

To demonstrate how the **VoxTour Widget** works, let's take a look at a self-guided audio tour of Amsterdam. Below is an example of how the widget can be embedded into a website, offering visitors an interactive experience of the city's iconic landmarks.

> **Try It Live:** Explore the **Amsterdam Walking Tour**, featuring narrated insights on must-visit locations like the Royal Palace of Amsterdam, Dam Square, Westerkerk, and the famous canals.

<div class="voxtour-widget-container">
    <iframe class="voxtour-widget"  id="widget-iframe" 
        src="https://widget.voxtour.ai/?apiKey=96f5b69a-6f16-4b36-ae05-b85a7dd728a6&tourId=02c2f25a-ccdd-4a2b-8f5e-d75ae63ef0b7">
    </iframe>
</div>

This widget allows users to:  
- Listen to **high-quality narrated stories** about Amsterdam’s history and culture.  
- Follow a **GPS-based tour** for a real-time exploration experience.  
- View images and descriptions of each **Point of Interest (POI)**.  
- Use **full-screen mode** for an app-like immersive experience.

---

## Full-Screen Mode: A Mobile App-Like Experience

One of the most powerful features of the VoxTour Widget is its full-screen mode, which transforms it into an immersive, app-like experience.

### What Does This Mean?

**Feels Like a Mobile App:** When users enter full-screen mode, the widget functions just like a dedicated app, eliminating distractions like browser tabs and toolbars.

**Fast and Smooth Performance:** The tour loads quickly and functions seamlessly, even in areas with **poor internet connectivity**.

**Add to Home Screen:** Visitors can **save the tour as an icon** on their smartphone’s home screen for easy access, just like a native app.

---

## Who Can Benefit from the VoxTour Widget?

- **Travel Bloggers** – Enrich articles with interactive tours of the places they write about.
- **Tourism Portals** – Provide engaging content for travelers researching destinations.
- **Hotels & Hospitality Businesses** – Offer guests on-site or nearby attraction tours.
- **Museums & Cultural Organizations** – Enhance visitor experiences with narrated exhibits.
- **Event Organizers** – Add location-based audio guides to festivals, fairs, and more.

---

## Trusted by Our Amazing Partners

We are proud to collaborate with incredible partners like **[TripsNotes.com](https://tripsnotes.com/listen-and-travel-free-audio-tours/)** , who have already integrated the VoxTour Widget into their platform. They love how this feature enhances user engagement and provides travelers with immersive, self-guided experiences. Their enthusiasm for our widget further proves its value in transforming travel-related content into an interactive journey!

---

## Transform Your Website with VoxTour Today

The **VoxTour Widget** brings destinations to life, offering a unique way to engage your audience with immersive, self-guided experiences. Whether you want to **enhance your blog, promote a city’s heritage, or provide travelers with rich audio storytelling**, this simple yet powerful tool is a game-changer.

📌 **Try it for yourself! Embed the VoxTour Widget today and give your audience an unforgettable travel experience!**

<script>
    window.addEventListener("message", function(event) {
      if (event.data && event.data.action === "vtwEnterFullScreen") {
        vtwEnterFullScreen();
      } else if (event.data && event.data.action === "vtwExitFullScreen") {
        vtwExitFullScreen();
      }
    }, false);

  function vtwEnterFullScreen() {
      let activeIframe = document.activeElement;
      if (!activeIframe || activeIframe.tagName !== 'IFRAME') {
          activeIframe = document.getElementById("widget-iframe");
      }
      if (activeIframe) {
          let container = activeIframe.parentNode;
          container.classList.add('voxtour-full-screen');
      }
  }

  function vtwExitFullScreen() {
      let activeIframe = document.activeElement;
      if (!activeIframe || activeIframe.tagName !== 'IFRAME') {
          activeIframe = document.getElementById("widget-iframe");
      }
      if (activeIframe) {
          let container = activeIframe.parentNode;
          container.classList.remove('voxtour-full-screen');
      }
  }
</script>