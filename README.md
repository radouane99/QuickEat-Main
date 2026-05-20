# 🍔 QuickEat - Plateforme Web de Livraison de Repas en Temps Réel

<p align="center">
  <img src="https://img.shields.io/badge/Architecture-Découplée%20%2FClien--Serveur-blue?style=for-the-badge" alt="Architecture">
  <img src="https://img.shields.io/badge/Spring%20Boot-3.x%20%20(Java%2017)-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Backend">
  <img src="https://img.shields.io/badge/React-18.x-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="Frontend">
  <img src="https://img.shields.io/badge/Real--Time-WebSockets%20%2F%20STOMP-orange?style=for-the-badge" alt="Temps Réel">
</p>

---

## 📌 À propos du Projet

**QuickEat** est une plateforme Full-Stack innovante conçue pour moderniser le secteur de la **FoodTech** au Maroc. Contrairement aux architectures web classiques, ce système repose sur une communication bidirectionnelle continue permettant une synchronisation instantanée et fluide entre trois acteurs majeurs : le **Client**, le **Restaurant**, et le **Livreur**.

Ce dépôt principal regroupe l'ensemble du projet via des **sous-modules Git** pour centraliser le code source.

---

## 📁 Structure du Projet (Monorepo via Submodules)

Ce projet est découpé en deux entités totalement autonomes qui communiquent via une API REST et des protocoles WebSockets :

* 📁 **[backend/]** : Développé avec **Spring Boot**, ce module gère la logique métier, la sécurité stricte via **Spring Security & JWT**, l'intégration des paiements avec **Stripe**, et le broker de messages pour le suivi GPS temps réel.
* 📁 **[frontend/]** : Développé avec **React.js** et stylisé avec **Tailwind CSS**, ce module offre une interface utilisateur moderne, réactive (Responsive), dotée de dashboards spécialisés par rôle et d'un système de tracking interactif.

---

## 🚀 Fonctionnalités Clés par Rôle

### 👤 Espace Client
* 🍕 **Menu Interactif :** Consultation des plats par catégories, recherche filtrée.
* 🛒 **Gestion du Panier :** Calcul dynamique des totaux.
* 💳 **Paiement Sécurisé :** Intégration de l'API Stripe (Carte bancaire) et option Cash à la livraison.
* 📍 **Suivi GPS en Temps Réel :** Visualisation en direct du déplacement du livreur sur une carte interactive après validation.
* ⭐ **Feedback & Évaluations :** Système de notation (Étoiles + Commentaires) du restaurant et du livreur dès la réception.

### 🏪 Espace Restaurant Partner
* 📊 **Tableau de Bord :** Statistiques des ventes et des commandes reçues.
* 🍔 **Gestion du Menu (CRUD) :** Ajout, modification de la disponibilité des plats en direct.
* 🔔 **Alertes Instantanées :** Notifications sonores/visuelles via WebSockets lors de la réception d'une nouvelle commande.

### 🛵 Espace Livreur (Coursier)
* 📦 **Gestion des Courses :** Consultation des commandes prêtes à être récupérées.
* 🗺️ **Simulation GPS :** Envoi automatique des coordonnées de géolocalisation toutes les 5 secondes au serveur pour notifier le client.

---

## 🛠️ Stack Technique

### Backend (API REST & WebSocket)
* **Langage :** Java 17
* **Framework Core :** Spring Boot 3.x
* **Sécurité :** Spring Security, Authentification Stateless via Tokens JWT (JSON Web Tokens)
* **Persistance :** Spring Data JPA / Hibernate
* **Base de Données :** MySQL
* **Temps Réel :** Spring WebSocket (Protocole STOMP over SockJS)

### Frontend (SPA)
* **Bibliothèque Principale :** React.js (Hooks, Context API pour l'état global)
* **Styling :** Tailwind CSS (Design Moderne & Ultra-Responsive)
* **Client HTTP :** Axios (Intercepteurs automatiques pour l'injection du Token JWT)
* **Cartographie :** Leaflet.js / React-Leaflet (pour le rendu de la carte GPS)

---

## ⚙️ Installation et Démarrage Rapide

### 1. Cloner le projet avec ses sous-modules
Puisque ce dépôt utilise des submodules Git, clonez le projet en utilisant la commande suivante :
```bash
git clone --recursive [https://github.com/radouane99/QuickEat-Main.git](https://github.com/radouane99/QuickEat-Main.git)
