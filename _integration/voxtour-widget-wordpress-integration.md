---
layout: default
title: VoxTour Widget WordPress Integration
parent_url: "https://support.voxtour.ai/api/integration.html"
order: 1
---

# VoxTour WordPress Widget Plugin – Installation & Usage Guide

The VoxTour plugin allows you to easily embed VoxTour audio guides on your website using a shortcode.

## 1. Install the Plugin

1. Download the **VoxTour Widget plugin (.zip)** provided by VoxTour.
2. In your WordPress dashboard go to:

**Plugins → Add New → Upload Plugin**

3. Upload the plugin `.zip` file.
4. Click **Install Now**.
5. Click **Activate Plugin**.

---

## 2. Enter Your VoxTour API Key

After activating the plugin:

1. Go to:

**Settings → VoxTour**

2. Paste the **API Key** provided by VoxTour.
3. Click **Save Changes**.

This key connects your site with the VoxTour service.

---

## 3. Insert a VoxTour Audio Guide into a Page or Post

You can display any VoxTour audio guide using the shortcode below:

```
[voxtour tour="TOUR_ID" locale="en"]
```

### Example

```
[voxtour tour="29b24f5b-5b55-42bd-9964-7ae51f1a877b" locale="en"]
```

Where:

| Parameter  | Description                                  |
| ---------- | -------------------------------------------- |
| **tour**   | The unique tour ID provided by VoxTour       |
| **locale** | Language of the tour (e.g. `en`, `ru`, etc.) |

---

## 4. Multiple Tours on One Page

You can insert multiple VoxTour widgets in the same post or page by adding multiple shortcodes:

```
[voxtour tour="TOUR_ID_1" locale="en"]

[voxtour tour="TOUR_ID_2" locale="en"]

[voxtour tour="TOUR_ID_3" locale="en"]
```

---

## 5. Fullscreen Mode

The VoxTour widget supports fullscreen playback.
Users can expand the audio guide to fullscreen directly from the player.

---

## 6. Analytics

The plugin automatically tracks widget loads for site analytics systems (such as Google Analytics or Google Tag Manager if installed).

---

## Need Help?

If you need tour IDs or API access, contact the VoxTour team.
