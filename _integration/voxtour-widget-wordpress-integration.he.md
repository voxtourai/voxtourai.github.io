---
layout: default
title: שילוב ווידג׳ט VoxTour עבור WordPress
parent_url: "https://support.voxtour.ai/api/integration.html"
order: 1
lang: he
---

# תוסף ווידג׳ט VoxTour ל-WordPress – מדריך התקנה ושימוש

התוסף VoxTour מאפשר לשלב בקלות מדריכי אודיו של VoxTour באתר שלך באמצעות shortcode.

## 1. התקנת התוסף

1. הורד את **תוסף VoxTour Widget (.zip)** שסופק על ידי VoxTour.
2. בלוח הבקרה של WordPress עבור אל:

**Plugins → Add New → Upload Plugin**

3. העלה את קובץ ה-`.zip` של התוסף.
4. לחץ על **Install Now**.
5. לחץ על **Activate Plugin**.

---

## 2. הזנת מפתח ה-API של VoxTour

לאחר הפעלת התוסף:

1. עבור אל:

**Settings → VoxTour**

2. הדבק את **מפתח ה-API** שסופק על ידי VoxTour.
3. לחץ על **Save Changes**.

מפתח זה מחבר את האתר שלך לשירות VoxTour.

---

## 3. הוספת מדריך אודיו של VoxTour לעמוד או לפוסט

ניתן להציג כל מדריך אודיו של VoxTour באמצעות ה-shortcode הבא:

[voxtour tour="TOUR_ID" locale="en"]

### דוגמה

[voxtour tour="29b24f5b-5b55-42bd-9964-7ae51f1a877b" locale="en"]

כאשר:

| Parameter  | תיאור                                                         |
| ---------- |---------------------------------------------------------------|
| **tour**   | מזהה הטור הייחודי שסופק על ידי VoxTour                        |
| **locale** | שפת הטור (לדוגמה `en`, `ru` וכו'). ברירת המחדל היא `en`      |

---

## 4. מספר טורים באותו עמוד

ניתן להוסיף מספר ווידג׳טים של VoxTour באותו פוסט או עמוד על ידי הוספת מספר shortcodes:

[voxtour tour="TOUR_ID_1" locale="en"]

[voxtour tour="TOUR_ID_2" locale="en"]

[voxtour tour="TOUR_ID_3" locale="en"]

---

## 5. מצב מסך מלא

ווידג׳ט VoxTour תומך בהפעלה במסך מלא.  
המשתמש יכול להרחיב את מדריך האודיו למסך מלא ישירות מהנגן.

---

## 6. אנליטיקה

התוסף עוקב אוטומטית אחר טעינת הווידג׳ט עבור מערכות אנליטיקה של האתר (כגון Google Analytics או Google Tag Manager אם מותקנים).

---

## צריכים עזרה?

אם אתם זקוקים למזהי טורים או לגישה ל-API, צרו קשר עם צוות VoxTour.