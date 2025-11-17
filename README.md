# **Project Management SaaS – Documentation du Projet**

## **Présentation du Projet**

Ce projet consiste à développer un **SaaS (Software as a Service)** de gestion de projet permettant aux équipes de suivre leurs tâches, issues, releases, tests et documentation au sein d’une plateforme centralisée.

Le système offre une interface intuitive en React ainsi qu’une API REST sécurisée en Node.js. Il est conçu pour être facilement extensible, collaboratif et adapté à la gestion agile.

---

# **Fonctionnalités du SaaS**

Le logiciel propose les modules suivants :

### **1. Authentification sécurisée**

* Création de compte
* Connexion JWT
* Gestion des rôles (admin, developer, tester)

### **2. Gestion des Issues (tickets)**

* Création, édition et suppression
* Types : bug, feature, task
* Priorités : low → critical
* Statuts : open → closed
* Assignation des membres

### **3. Gestion des Tâches**

* Lien direct avec les issues
* Estimation & temps passé
* Suivi des statuts : todo → done

### **4. Module Releases**

* Planification des versions
* Association d’issues à une release
* Notes de release

### **5. Module Tests**

* Tests unitaires, intégration ou manuels
* Statuts : passed, failed, pending
* Documentation des résultats

### **6. Documentation intégrée**

* Documentation technique, utilisateur, admin
* Versioning intégré

### **7. Tableau de bord**

* Vue synthétique des issues, tâches, releases et tests
* Indicateurs de progression

### **8. Extensions prévues (Sprint 4 – optionnel)**

* Vue Kanban
* Notifications
* Intégration Git
* Améliorations UI/UX

---

# **Architecture du SaaS**

Le système est divisé en deux grandes parties :

## **Frontend**

* **React 18+ avec Vite**
* **Material-UI**
* **React Router v6**
* **Context API & Reducers**
* **Axios**

## **Backend**

* **Node.js 22 + Express.js**
* **JWT Authentication**
* **Sequelize ORM (PostgreSQL)**
* **express-validator, bcrypt, dotenv**

## **Base de données**

* **PostgreSQL 15**
* Migrations avec Sequelize CLI

---

# **Arborescence Globale**

```
/frontend
  /src
    /components
    /pages
    /services
    /contexts
    /utils
    /assets
    App.js
    main.jsx

/backend
  /src
    /controllers
    /models
    /routes
    /middlewares
    /config
    /utils
    server.js

/release
  README.md
  Backlog.md
  Sprint0.md
  Tasks0.md
  Release.md
  Documentation.md
```

---

# **Planification des Sprints**

| Sprint                   | Modules livrés                                                                       | Objectif                                  |
| ------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------- |
| **Sprint 1**             | Authentification, Structure du projet, Base de données, Gestion partielle des Issues | Mettre en place les fondations techniques |
| **Sprint 2**             | Gestion complète des Issues et Tâches, Dashboard, Navigation                         | Obtenir un MVP fonctionnel                |
| **Sprint 3**             | Releases, Tests, Documentation, Rapports                                             | Finalisation des fonctionnalités clés     |
| **Sprint 4 (optionnel)** | UX/UI, Notifications, Git Integration, Vue Kanban                                    | Améliorations et fonctionnalités avancées |

---

# **Technologies utilisées**

| Domaine         | Outils                                      |
| --------------- | ------------------------------------------- |
| Frontend        | React 18+, Vite, MUI, Axios, React Router   |
| Backend         | Node.js, Express.js, JWT, express-validator |
| Base de données | PostgreSQL 15, Sequelize ORM                |
| Tests           | Jest, Supertest, Cypress                    |
| Documentation   | Markdown, Swagger/OpenAPI 3                 |
| Outils          | GitHub, VSCode, Slack                       |

---

# **Équipe du Projet**

| Nom                 | Rôle                                            |
| ------------------- | ----------------------------------------------- |
| **Saif Amine**      | Full-Stack Developer, Scrum Master              |
| **Ameziane Adnane** | Full-Stack Developer, Référent Frontend / UI-UX |
| **Chelh Monir**     | Full-Stack Developer                            |

---

# **Livrables de la Release**

* **Sprint0.md** – Phase préparatoire
* **Tasks0.md** – Tâches du sprint 0
* **Backlog.md** – User stories
* **Release.md** – Description des versions
* **Documentation.md** – Documentation du SaaS

Chaque sprint produit une **release documentée**, incluant :

* Modules livrés
* Tests effectués
* Rétrospective
* État du backlog

---

# **Objectif du Projet**

Ce SaaS a pour mission d’aider les équipes de développement à :

* Organiser leur travail
* Planifier leurs versions
* Suivre leurs issues et tâches
* Gérer leurs tests
* Documenter leur projet

L’objectif final est de fournir une **solution complète, scalable et intuitive** pour la gestion de projets agiles.

---

# **Installation**

## **Backend**

```bash
cd backend
npm install
npm run dev
```

## **Frontend**

```bash
cd frontend
npm install
npm run dev
```

## **Configuration**

Créer un fichier `.env` à la racine du backend :

```
DB_HOST=localhost
DB_USER=projet_user
DB_PASS=xxxxx
DB_NAME=gestion_projet_db
JWT_SECRET=xxxx
PORT=5000
```

---

# **Statut du Projet**

* **Version actuelle :** 1.1
* **Dernière mise à jour :** 22/10/2025
* **Statut :** En développement
