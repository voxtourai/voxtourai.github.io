---
layout: default
title: שילוב VoxTour
parent: API & Widgets
description: שילוב מדריכי האודיו של VoxTour באתרים, אפליקציות ופלטפורמות דיגיטליות.
lang: he
---

# שילוב VoxTour

שילובי VoxTour מאפשרים למפתחים, שותפים ופלטפורמות תוכן לשלב מדריכי אודיו אינטראקטיביים ישירות באתרי האינטרנט, באפליקציות ובחוויות הדיגיטליות שלהם.

באמצעות הווידג'טים, ה-API והכלים של פלטפורמת VoxTour ניתן להוסיף בקלות סיורי אודיו חווייתיים לאתרי תיירות, פורטלי תיירות, בלוגים, אפליקציות מובייל ומוצרים דיגיטליים נוספים.

שילובי VoxTour תוכננו להיות קלים ליישום תוך שמירה על גמישות למגוון רחב של שימושים — מהטמעת מדריך אודיו יחיד בפוסט בבלוג ועד הפעלת פלטפורמות תיירות גדולות.

{% assign active_lang = site.active_lang | default: site.default_lang %}
{% assign sorted_items = site.integration | sort: 'order' %}
{% if active_lang == site.default_lang %}
{% assign filtered_items = sorted_items | where_exp: "item", "item.lang == nil or item.lang == active_lang" %}
{% else %}
{% assign filtered_items = sorted_items | where: "lang", active_lang %}
{% endif %}
{% for item in filtered_items %}

<details>
    <summary>{{ item.title }}</summary>
    {{item.content}}
    <a href="{{ item.url }}"><img alt="Share" src="/assets/images/share-icon-20x20.jpg"></a>
</details>

{% endfor %}