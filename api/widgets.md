---
layout: default
title: Widgets
parent: API & Widgets
description: VoxTour.ai provides a powerful API for integrating AI-powered audio guides and travel experiences into applications, websites, and services. Our API enables seamless access to high-quality, location-based storytelling, allowing users to explore destinations with engaging narratives, historical insights, and personalized recommendations.
---

<style>
    html, body {
        height: 100%;
        margin: 0;
    }
    .voxtour-desctop-widget-container {
        width: 770px;
        height: 700px;
        border: 3px solid #aaa;
        border-radius: 10px;
        padding: 5px;
    }
    .voxtour-mobile-widget-container {
        width: 400px;
        height: 700px;
        border: 3px solid #aaa;
        border-radius: 6px;
        padding: 5px;
        overflow: hidden;
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

<details>
    <summary>Desktop Widget (770px x 700px)</summary>
<div class="voxtour-desctop-widget-container">
    <iframe class="voxtour-widget"  id="desktop-iframe" 
        src="https://widget.voxtour.ai/?apiKey=96f5b69a-6f16-4b36-ae05-b85a7dd728a6&tourId=89c0e34d-8d32-402d-9752-11a49ef04f73">
    </iframe>
</div>
</details>

<details>
    <summary>Mobile Widget (400px x 700px)</summary>
<div class="voxtour-mobile-widget-container">
    <iframe class="voxtour-widget"  id="mobile-iframe" 
        src="https://widget.voxtour.ai/?apiKey=96f5b69a-6f16-4b36-ae05-b85a7dd728a6&tourId=89c0e34d-8d32-402d-9752-11a49ef04f73">
    </iframe>   
</div>
</details>

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
          activeIframe = document.getElementById("desktop-iframe") || document.getElementById("mobile-iframe");
      }
      if (activeIframe) {
          let container = activeIframe.parentNode;
          container.classList.add('voxtour-full-screen');
      }
  }

  function vtwExitFullScreen() {
      let activeIframe = document.activeElement;
      if (!activeIframe || activeIframe.tagName !== 'IFRAME') {
          activeIframe = document.getElementById("desktop-iframe") || document.getElementById("mobile-iframe");
      }
      if (activeIframe) {
          let container = activeIframe.parentNode;
          container.classList.remove('voxtour-full-screen');
      }
  }
</script>