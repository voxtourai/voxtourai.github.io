---
layout: default
title: Intégration du widget VoxTour pour WordPress
parent_url: "https://support.voxtour.ai/api/integration.html"
order: 1
lang: fr
---

# Plugin Widget VoxTour pour WordPress – Guide d’installation et d’utilisation

Le plugin VoxTour vous permet d’intégrer facilement des audioguides VoxTour sur votre site web à l’aide d’un shortcode.

## 1. Installer le plugin

1. Téléchargez le **plugin VoxTour Widget (.zip)** fourni par VoxTour.
2. Dans le tableau de bord WordPress, allez dans :

**Plugins → Add New → Upload Plugin**

3. Téléversez le fichier `.zip` du plugin.
4. Cliquez sur **Install Now**.
5. Cliquez sur **Activate Plugin**.

---

## 2. Entrer votre clé API VoxTour

Après l’activation du plugin :

1. Allez dans :

**Settings → VoxTour**

2. Collez la **clé API** fournie par VoxTour.
3. Cliquez sur **Save Changes**.

Cette clé connecte votre site au service VoxTour.

---

## 3. Insérer un audioguide VoxTour dans une page ou un article

Vous pouvez afficher n’importe quel audioguide VoxTour en utilisant le shortcode ci-dessous :

[voxtour tour="TOUR_ID" locale="en"]

### Exemple

[voxtour tour="29b24f5b-5b55-42bd-9964-7ae51f1a877b" locale="en"]

Où :

| Parameter  | Description                                                  |
| ---------- |--------------------------------------------------------------|
| **tour**   | L’identifiant unique du tour fourni par VoxTour             |
| **locale** | Langue du tour (par exemple `en`, `ru`, etc.). Par défaut `en` |

---

## 4. Plusieurs tours sur une même page

Vous pouvez insérer plusieurs widgets VoxTour dans un même article ou une même page en ajoutant plusieurs shortcodes :

[voxtour tour="TOUR_ID_1" locale="en"]

[voxtour tour="TOUR_ID_2" locale="en"]

[voxtour tour="TOUR_ID_3" locale="en"]

---

## 5. Mode plein écran

Le widget VoxTour prend en charge la lecture en plein écran.  
Les utilisateurs peuvent agrandir l’audioguide en plein écran directement depuis le lecteur.

---

## 6. Analytique

Le plugin suit automatiquement les chargements du widget pour les systèmes d’analytique du site (comme Google Analytics ou Google Tag Manager s’ils sont installés).

---

## Besoin d’aide ?

Si vous avez besoin d’identifiants de tours ou d’un accès API, contactez l’équipe VoxTour.