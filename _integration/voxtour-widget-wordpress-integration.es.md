---
layout: default
title: Integración del Widget VoxTour para WordPress
parent_url: "https://support.voxtour.ai/api/integration.html"
order: 1
lang: es 
---

# Plugin del Widget VoxTour para WordPress – Guía de Instalación y Uso

El plugin VoxTour le permite incrustar fácilmente guías de audio de VoxTour en su sitio web utilizando un shortcode.

## 1. Instalar el Plugin

1. Descargue el **plugin VoxTour Widget (.zip)** proporcionado por VoxTour.
2. En el panel de administración de WordPress vaya a:

**Plugins → Añadir nuevo → Subir plugin**

3. Suba el archivo `.zip` del plugin.
4. Haga clic en **Instalar ahora**.
5. Haga clic en **Activar plugin**.

---

## 2. Introducir su clave API de VoxTour

Después de activar el plugin:

1. Vaya a:

**Ajustes → VoxTour**

2. Pegue la **clave API** proporcionada por VoxTour.
3. Haga clic en **Guardar cambios**.

Esta clave conecta su sitio con el servicio de VoxTour.

---

## 3. Insertar una guía de audio de VoxTour en una página o entrada

Puede mostrar cualquier guía de audio de VoxTour utilizando el siguiente shortcode:

```
[voxtour tour="TOUR_ID" locale="en"]
```

### Ejemplo


```
[voxtour tour="29b24f5b-5b55-42bd-9964-7ae51f1a877b" locale="es"]
```


Dónde:

| Parámetro  | Descripción                                                   |
| ---------- |---------------------------------------------------------------|
| **tour**   | El ID único del tour proporcionado por VoxTour                |
| **locale** | Idioma del tour (por ejemplo `en`, `ru`, etc.). Por defecto `en` |

---

## 4. Múltiples tours en una misma página

Puede insertar múltiples widgets de VoxTour en la misma entrada o página añadiendo varios shortcodes:

```
[voxtour tour="TOUR_ID_1" locale="en"]

[voxtour tour="TOUR_ID_2" locale="en"]

[voxtour tour="TOUR_ID_3" locale="en"]
```

---

## 5. Modo de pantalla completa

El widget de VoxTour admite reproducción en pantalla completa.  
Los usuarios pueden ampliar la guía de audio a pantalla completa directamente desde el reproductor.

---

## 6. Analítica

El plugin rastrea automáticamente las cargas del widget para sistemas de analítica del sitio (como Google Analytics o Google Tag Manager si están instalados).

---

## ¿Necesita ayuda?

Si necesita IDs de tours o acceso a la API, contacte con el equipo de VoxTour.