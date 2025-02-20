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
        width: 900px;
        height: 700px;
        border: 3px solid #aaa;
        border-radius: 10px;
        padding: 5px;
    }
    .voxtour-mobile-widget-container {
        width: 400px;
        height: 700px;
        border: 3px solid #aaa;
        border-radius: 10px;
        padding: 5px;
        overflow: hidden;
    }
    .voxtour-widget {
        width: 100%;
        height: 100%;
        border: none;
        touch-action: pan-x;
        pointer-events: auto;
    }
</style>

<details>
    <summary>Desktop Widget (900px x 700px)</summary>
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
    function enableParentScroll(iframe) {
        let lastTouchY = 0;

        iframe.addEventListener("touchstart", function(event) {
            const touch = event.touches[0];
            iframe.dataset.startX = touch.clientX;
            iframe.dataset.startY = touch.clientY;
            lastTouchY = touch.clientY;
        });

        iframe.addEventListener("touchmove", function(event) {
            const touch = event.touches[0];
            const deltaX = Math.abs(touch.clientX - iframe.dataset.startX);
            const deltaY = Math.abs(touch.clientY - iframe.dataset.startY);

            if (deltaY > deltaX) {
                event.stopPropagation();
                event.preventDefault();
                let scrollAmount = lastTouchY - touch.clientY;
                window.scrollBy(0, scrollAmount);
                lastTouchY = touch.clientY;
            }
        }, { passive: false });
    }

    document.addEventListener("DOMContentLoaded", function () {
        const desktopIframe = document.getElementById("desktop-iframe");
        const mobileIframe = document.getElementById("mobile-iframe");

        enableParentScroll(desktopIframe);
        enableParentScroll(mobileIframe);
    });
</script>