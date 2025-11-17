# **Release – Suivi des Versions du SaaS de Gestion de Projet**

Ce document liste l’ensemble des versions livrées dans le cadre du projet, selon la méthodologie agile SCRUM.
Chaque release correspond à un sprint et décrit :

* Les fonctionnalités livrées
* Les tests réalisés
* Les améliorations
* Les tickets résolus
* Les limites connues

---

# **Release 0 – Sprint 0 : Phase Préparatoire**

**Version :** 0.1
**Date :** 22/10/2025
**Statut :** Terminé

## **Objectif**

Mettre en place les bases du projet et préparer le cadre technique.

## **Livrables**

* Configuration complète des dépôts Git
* Documentation du Sprint 0 (`Sprint0.md`, `Tasks0.md`)
* Backlog initial (`Backlog.md`)
* Stack technique définie
* Architecture frontend + backend
* Planning des sprints
* Modèle de données initial

## **Tests effectués**

* Vérification manuelle de la structure Git
* Vérification de la cohérence du backlog
* Validation de l’architecture auprès de l’équipe

## **Limites**

Aucune fonctionnalité applicative livrée (phase préparatoire uniquement).

---

# **Release 1 – Sprint 1 : Fondations & Authentification**

**Version :** 1.0
**Période :** 25/10 → 05/11/2025

## **Objectif**

Mettre en place les fondations techniques du SaaS et commencer les fonctionnalités essentielles.

## **Fonctionnalités livrées**

* Mise en place du backend Express
* Mise en place du frontend React + Vite
* Configuration PostgreSQL et Sequelize
* Authentification JWT
* Création d’un compte utilisateur
* Connexion utilisateur
* Gestion partielle des Issues :

  * Création
  * Liste des issues
  * Détails d’une issue

## **Tests effectués**

* Tests API manuels via Thunder Client
* Tests unitaires backend (Jest + Supertest)
* Tests frontend basiques (Jest)
* Vérification des flux d’authentification

## **Améliorations prévues**

* Validation renforcée
* Gestion avancée des permissions
* UI améliorée pour les issues

## **Limites**

* Pas encore de gestion des tâches
* Pas de dashboard
* Pas de release management

---

# **Release 2 – Sprint 2 : MVP Fonctionnel**

**Version :** 2.0
**Période :** 06/11 → 20/11/2025

## **Objectif**

Obtenir un MVP complet et utilisable du SaaS.

## **Fonctionnalités livrées**

* Gestion complète des Issues
* Gestion des Tâches (CRUD + statut + assignation)
* Dashboard utilisateur
* Navigation frontend améliorée
* Filtrage et tri des issues
* Gestion des priorités et statuts
* Suivi du temps (estimation / temps passé)

## **Tests effectués**

* Tests d’intégration backend
* Tests d’affichage des pages React
* Automatisation partielle via Cypress
* Validation UI/UX

## **Améliorations prévues**

* Design plus moderne
* Ajout de métriques avancées
* Gestion des releases

## **Limites**

* Pas encore de module release
* Pas encore de module test
* Documentation partielle

---

# **Release 3 – Sprint 3 : Finalisation & Qualité Logicielle**

**Version :** 3.0
**Période :** 04/12 → 16/12/2025

## **Objectif**

Compléter toutes les fonctionnalités principales et assurer la qualité du SaaS.

## **Fonctionnalités livrées**

* Module Releases (versions logicielles)
* Association d’issues à une release
* Module Tests (unitaire, intégration, manuel)
* Documentation intégrée (technique / utilisateur / admin)
* Génération de rapports de sprint
* Export des données
* Améliorations UI/UX générales

## **Tests effectués**

* Tests unitaires & intégration avancés
* Scénarios E2E sous Cypress
* Tests manuels de bout en bout
* Vérification de la compatibilité navigateurs

## **Améliorations prévues**

* Notifications temps réel
* Vue Kanban
* Intégration Git

## **Limites**

* Pas encore de notifications
* Pas encore de collaboration en temps réel

---

# **Release 4 – Sprint 4 (Optionnel) : Optimisations & Extensions**

**Version :** 4.0
**Période :** À définir (optionnel)

## **Objectif**

Ajouter les fonctionnalités avancées et améliorer l’expérience utilisateur.

## **Fonctionnalités prévues**

* Vue Kanban complète
* Intégration GitHub/GitLab pour suivre les commits
* Système de notifications
* Optimisations UI/UX
* Performances améliorées

---

# **Suivi de Version**

| Version | Sprint   | Date       | Statut      |
| ------- | -------- | ---------- | ----------- |
| **0.1** | Sprint 0 | 22/10/2025 | Terminé     |
| **1.0** | Sprint 1 | 05/11/2025 | Terminé     |
| **2.0** | Sprint 2 | 20/11/2025 | Prévu       |
| **3.0** | Sprint 3 | 16/12/2025 | Prévu       |
| **4.0** | Sprint 4 | Optionnel  | À confirmer |

