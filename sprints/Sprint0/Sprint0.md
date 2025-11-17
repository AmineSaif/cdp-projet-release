# **Sprint 0 - Phase Préparatoire**

**Période :** du 15 Octobre jusqu'au mercredi 22 Octobre
**Équipe :** Saif Amine, Ameziane Adnane, Chelh Monir

---

## **Objectifs du Sprint 0**

Le Sprint 0 vise à poser les fondations solides du projet avant de commencer le développement. Les objectifs principaux sont :

1. Mise en place de l'environnement de travail
2. Définition de l'architecture technique
3. Création du backlog initial
4. Organisation des outils de communication et de gestion
5. Planification des sprints suivants

---

## **Tâches Réalisées**

### **1. Organisation de l'Équipe**

**Rôles définis :**

* **Product Owner :** Professeur – Responsable du backlog et des priorités
* **Équipe de développement :** Saif Amine, Ameziane Adnane, Chelh Monir

  * Développement Full-Stack
  * Gestion agile partagée
  * Documentation et tests

**Communication :**

* Canal Slack créé et configuré
* Réunions quotidiennes : 15 min chaque soir à 19h
* Rétrospective de sprint : dernier jour de chaque sprint

---

### **2. Configuration des Dépôts Git**

**Dépôt Développement :**

* Repository : `cdp-project-developpement`
* Branches :

  * `main` : stable
  * `develop` : développement
  * `feature/*` : nouvelles fonctionnalités
  * `bugfix/*` : corrections

**Dépôt Release :**

* Repository : `cdp-projet-release`
* Structure :

  * README.md
  * Backlog.md
  * Sprint0.md
  * Tasks0.md
  * Release.md
  * Documentation.md

**Convention de commits :**

* `feat:` nouvelle fonctionnalité
* `fix:` correction de bug
* `docs:` documentation
* `refactor:` refactorisation
* `test:` tests

---

### **3. Stack Technique Choisie**

#### **Frontend**

* React.js 18+ (Vite)
* JavaScript / TypeScript
* Material UI
* React Router v6
* Context API + useReducer
* Axios

#### **Backend**

* Node.js + Express.js
* JSON Web Tokens (JWT)
* express-validator
* Bcrypt
* Sequelize ORM

#### **Base de données**

* PostgreSQL 15+
* Sequelize CLI

#### **Outils**

* GitHub
* VS Code
* ESLint, Prettier, GitLens
* Documentation avec Markdown + JSDoc

---

## **4. Architecture du Projet**

### **Structure Frontend**

```
/src
  /components
  /pages
  /services
  /contexts
  /utils
  /assets
  App.js
  index.js
```

### **Structure Backend**

```
/src
  /controllers
  /models
  /routes
  /middlewares
  /config
  /utils
  server.js
```

---

## **5. Modèle de Données Initial**

### **Entités : Issues**

* id
* titre
* description
* type (bug, feature, task)
* priorité
* statut
* créateur_id
* assigne_a_id
* date_creation
* date_mise_a_jour

### **Entités : Tasks**

* id
* titre
* description
* statut
* issue_id
* assigne_a_id
* estimation
* temps_passe
* date_debut
* date_fin

### **Entités : Release**

* id
* version
* nom
* description
* date_release
* statut
* notes_release

### **Entités : Tests**

* id
* nom
* description
* type
* statut
* issue_id
* date_execution

### **Entités : Users**

* id
* nom
* email
* mot_de_passe
* rôle

### **Documentation**

* id
* titre
* contenu
* type
* version
* date_creation

---

## **6. Backlog Initial (Extrait)**

### **Sprint 1 – Priorité Haute**

* Créer un compte & se connecter
* Créer une issue
* Lister les issues
* Voir le détail d’une issue
* Créer une tâche liée
* Modifier le statut d’une tâche

### **Sprint 2 – Priorité Moyenne**

* Créer une release
* Associer des issues à une release
* Créer un test
* Exécuter et documenter un test

### **Sprint 3 – Priorité Basse**

* Créer de la documentation
* Rapport de sprint
* Statistiques
* Export des données

---

## **7. Environnement de Développement**

### **Frontend**

```bash
npm create vite@latest frontend -- --template react
cd frontend
npm install

npm install @mui/material @emotion/react @emotion/styled
npm install react-router-dom axios react-hook-form
```

### **Backend**

```bash
mkdir backend && cd backend
npm init -y

npm install express pg sequelize jsonwebtoken bcrypt cors dotenv express-validator
npm install --save-dev nodemon
```

### **Base PostgreSQL**

* BDD : `gestion_projet_db`
* User : `projet_user`
* Port : 5432

---

## **8. Planning des Sprints**

| Sprint                   | Modules livrés                                                                       | Objectif                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| **Sprint 1**             | Authentification, Structure du projet, Base de données, Gestion partielle des Issues | Mettre en place les fondations techniques et les fonctionnalités essentielles |
| **Sprint 2**             | Gestion complète des Issues et Tâches, Dashboard, Navigation                         | Avoir un MVP fonctionnel                                                      |
| **Sprint 3**             | Releases, Tests, Documentation, Rapports                                             | Finaliser les fonctionnalités principales                                     |
| **Sprint 4 (optionnel)** | UX/UI, Notifications, Git intégration, Vue Kanban                                    | Optimisations et extensions                                                   |

---

## **Definition of Done (DoD)**

* Code fonctionnel
* Tests réalisés
* Code reviewé
* Documentation mise à jour
* Commit et push
* Merge sur `develop`

---

## **Conventions de Code & Git**

### **Code**

* Anglais pour le code, français pour la doc
* 2 espaces indentation
* Point-virgule obligatoire

### **Git**

* Commits petits et fréquents
* Messages clairs
* Pull request obligatoire
* 1 review minimum

---

## **Workflow**

1. Créer une branche depuis `develop`
2. Développer
3. Tester
4. Commit + push
5. Pull Request
6. Review
7. Merge

---

## **Prochaines Étapes (Sprint 1)**

* Initialisation des projets
* Setup base PostgreSQL
* Authentification JWT
* Routes API de base
* Composants React de base
* Gestion des issues

---

## **Membres de l'Équipe**

| Nom                 | Responsabilités                                                                  |
| ------------------- | -------------------------------------------------------------------------------- |
| **Saif Amine**      | Développement Full-Stack, Scrum Master (communication & distribution des tâches) |
| **Ameziane Adnane** | Développement Full-Stack, Référent Frontend / UI-UX                              |
| **Chelh Monir**     | Développement Full-Stack                                                         |

---

**Date de rédaction :** 22/10/2025
**Version :** 1.1
**Statut :** Terminé

