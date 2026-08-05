# Portfolio – Senior Software Engineer

Bonjour,

Merci pour votre intérêt.  
Voici une sélection de projets et d’expériences représentatives de ma manière de travailler :  
**livrer vite sans casser**, clarifier le métier, structurer le domaine quand c’est utile, et garder un **focus constant sur l’impact en production**.

---

## 🟦 Orders App — SaaS Orders Management (Angular 17 + .NET 8 + Keycloak)
**Lien :** https://github.com/mpersonnic/Orders

Application SaaS moderne construite en architecture hexagonale, avec un front Angular Material et une authentification Keycloak.
Je suis actuellement en train de travailler sur la partie Front pour passer les commandes autrement que par Postman.

### Points clés
- **Architecture hexagonale** : séparation claire domaine / application / infrastructure
- **CQRS : Mis en place à titre de démonstration
- **Approche pragmatique** : baby steps, itérations rapides, fonctionnalités livrables  
- **Sécurité & Auth** : Keycloak, JWT, Gateway, RBAC  
- **Qualité** : structure modulaire, tests unitaires ciblés, CI GitHub Actions  
- **UX SaaS** : dark theme, tables Material avancées
- **Observabilité** : logs structurés, gestion d’erreurs front/back (à venir)
- A venir : Dockerisation des trois applications (angular, .Net, Keycloak) et orchestrastion avec Docker Compose

---

## 🟪 RetroGalerie — ASP.NET MVC + Razor (Clean Architecture légère) + Chat IA (Ollama)
**Lien :** https://github.com/mpersonnic/RetroGalerie

Application ASP.NET MVC (.Net 10) avec Razor Views, orientée **gestion de collections de jeux rétro**.  
Le projet met l’accent sur une architecture claire, une UI dynamique côté serveur et une logique métier explicite.
Outre la collection de jeux possédés, l'appli permet de saisir les "jeux que souhaite voir entrer la collection".

### Points clés
- **ASP.NET MVC + Razor** : rendu serveur, vues fortement typées, logique claire et maintenable  
- **Modèle métier structuré** : Consoles, Jeux, agrégations, totaux, règles simples mais explicites  
- **UI dynamique** : collapses Bootstrap, interactions JS légères, affichage conditionnel  
- **Razor Views propres** : composants réutilisables, code lisible, séparation claire des responsabilités  
- **Clean Architecture légère** : Domain / Services / Controllers / Views  
- **Qualité pragmatique** : code simple, lisible, orienté métier  
- **Exemple concret** :  
  - tableau récapitulatif des consoles  
  - calcul du total de jeux  
  - affichage dynamique des jeux par console  
  - cartes Bootstrap avec images, titres, navigation  
  - gestion d’état (collapse ouvert/fermé) via JS

# RetroGalerie : Chatbot IA:

RetroGalerie.AI est une API IA en **.NET 8 Minimal API** qui combine :
- un modèle IA local via **Ollama**
- un système de **RAG (Retrieval-Augmented Generation)** connecté à la base RetroGalerie

L’objectif : permettre un chatbot capable de répondre avec précision sur les jeux rétro présent dans la collection: listes de jeux, consoles, variantes FRA, états, éditions, etc.

---

## ✨ Fonctionnalités

- Chat IA (modèle local Ollama)
- **RAG** : recherche dans la base RetroGalerie + génération IA
- Architecture propre : Domain / Application / Infrastructure / API
- Endpoints Minimal API

---

## 🔍 RAG : comment ça marche?

1. L’utilisateur pose une question  
2. Le service de retrieval analyse la requête  
3. Recherche dans la base RetroGalerie (EF Core)  
4. Les données trouvées sont injectées dans le prompt  
5. Le modèle IA génère une réponse enrichie et exacte

Ce mécanisme permet d’éviter les hallucinations et de fournir des réponses basées sur les données réelles du projet.
## Installation

### 1. Installer Ollama
 - **Lien :** https://ollama.com/download
 - Lancer `ollama pull llama3` dans un terminal afin de récupérer un modèle LLM


### 2. Configurer l’API
Modifier `appsettings.json` :

```json
{
  "Ollama": {
    "BaseUrl": "http://localhost:11434",
    "Model": "llama3"
  },
  "ConnectionStrings": {
    "RetroGalerie": "Server=...;Database=RetroGalerie;..."
  }
}
```
Ce projet illustre une approche **simple et orientée métier** :  
livrer vite, clarifier le domaine, éviter la complexité inutile, et garder une UI lisible et efficace.



---
## 🟪 MonAppliSécurisée — ASP.NET Core + Microsoft Identity
**Lien :** https://github.com/mpersonnic/MonAppliSecurisee

Application de TESTS ASP.NET Core testant Microsoft Identity pour gérer l’authentification, les rôles et la sécurité.
Le projet sert de base pour toute application nécessitant un système d’identités moderne.

###Points clés
- Microsoft Identity : inscription, connexion, rôles, reset password
- Sécurité : cookies protégés, hashing, anti-forgery, HTTPS/HSTS
- EF Core : migrations, persistance SQL Server / SQLite
- Razor Pages : pages d’authentification personnalisables
- Base réutilisable : idéale pour démarrer une app sécurisée

## 🛠️ Stack & outils
- **Langages** : C# .NET 8, ASP.NET MVC + Razor 
- **Architecture** : Clean Architecture, modular monolith  
- **BDD** : SQL Server
- **CI/CD** : GitHub Actions, CD progressif  
- **Observabilité** : logs structurés, métriques, traces (à venir)

---

Merci pour votre lecture.  
N’hésitez pas à me contacter pour toute question ou pour approfondir un sujet.
