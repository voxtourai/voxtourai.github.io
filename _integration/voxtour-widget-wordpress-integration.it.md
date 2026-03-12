---
layout: default
title: Integrazione del Widget VoxTour per WordPress
parent_url: "https://support.voxtour.ai/api/integration.html"
order: 1
lang: it
---

# Plugin Widget VoxTour per WordPress – Guida all’Installazione e all’Uso

Il plugin VoxTour consente di incorporare facilmente le audioguide VoxTour nel tuo sito web utilizzando uno shortcode.

## 1. Installare il Plugin

1. Scarica il **plugin VoxTour Widget (.zip)** fornito da VoxTour.
2. Nel pannello di amministrazione di WordPress vai a:

**Plugins → Add New → Upload Plugin**

3. Carica il file `.zip` del plugin.
4. Clicca su **Install Now**.
5. Clicca su **Activate Plugin**.

---

## 2. Inserire la tua chiave API VoxTour

Dopo aver attivato il plugin:

1. Vai a:

**Settings → VoxTour**

2. Incolla la **API Key** fornita da VoxTour.
3. Clicca su **Save Changes**.

Questa chiave collega il tuo sito al servizio VoxTour.

---

## 3. Inserire una guida audio VoxTour in una pagina o in un articolo

Puoi visualizzare qualsiasi audioguida VoxTour utilizzando lo shortcode seguente:

[voxtour tour="TOUR_ID" locale="en"]

### Esempio

[voxtour tour="29b24f5b-5b55-42bd-9964-7ae51f1a877b" locale="en"]

Dove:

| Parameter  | Descrizione                                                   |
| ---------- |---------------------------------------------------------------|
| **tour**   | L’ID univoco del tour fornito da VoxTour                      |
| **locale** | Lingua del tour (es. `en`, `ru`, ecc.). Di default `en`       |

---

## 4. Più tour nella stessa pagina

Puoi inserire più widget VoxTour nello stesso articolo o pagina aggiungendo più shortcode:

[voxtour tour="TOUR_ID_1" locale="en"]

[voxtour tour="TOUR_ID_2" locale="en"]

[voxtour tour="TOUR_ID_3" locale="en"]

---

## 5. Modalità schermo intero

Il widget VoxTour supporta la riproduzione a schermo intero.  
Gli utenti possono espandere l’audioguida a schermo intero direttamente dal player.

---

## 6. Analitica

Il plugin traccia automaticamente i caricamenti del widget per i sistemi di analisi del sito (come Google Analytics o Google Tag Manager se installati).

---

## Serve aiuto?

Se hai bisogno degli ID dei tour o dell’accesso API, contatta il team VoxTour.