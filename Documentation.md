# **Documentation – Project Management SaaS**

Ce document regroupe la documentation principale du projet :

* Documentation technique
* Documentation utilisateur
* Documentation administrateur
* Informations d’installation et de configuration
* Structure générale du code
* API overview

---

# **1. Présentation du SaaS**

Le **Project Management SaaS** est une plateforme web permettant aux équipes de gérer :

* leurs **issues**
* leurs **tâches**
* leurs **releases**
* leurs **tests**
* leur **documentation**
* leur **dashboard**

Il est conçu pour fournir une solution complète, moderne et intuitive pour gérer un projet logiciel en mode agile.

---

# **2. Architecture du Projet**

Le SaaS est organisé en **architecture Frontend / Backend séparée**, communiquant via une API REST sécurisée.

---

## **2.1. Frontend**

### **Technologies**

* React 18 (Vite)
* Material-UI
* Axios
* Context API / Reducer
* React Router v6

### **Objectif**

Fournir une interface moderne, rapide et intuitive.

### **Structure**

```
/src
  /components
  /pages
  /services
  /contexts
  /utils
  /assets
  App.js
  main.jsx
```

### **Fonctionnalités principales**

* Authentification (login / register)
* Dashboard
* CRUD Issues & Tasks
* Releases viewer
* Test management UI
* Documentation interface

---

## **2.2. Backend**

### **Technologies**

* Node.js 22
* Express.js 5
* Sequelize ORM
* JWT Auth
* express-validator
* bcrypt
* cors, dotenv

### **Structure**

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

### **Fonctionnalités**

* API REST sécurisée
* Authentification JWT
* Gestion Users / Issues / Tasks / Releases / Tests
* Validation des requêtes
* Hashage des mots de passe

---

## **2.3. Base de données**

**SGBD : PostgreSQL 15**

### **Tables principales**

* **users** (roles : admin, developer, tester)
* **issues**
* **tasks**
* **releases**
* **tests**
* **documentation**

### **Relations**

* 1 issue → N tasks
* 1 release → N issues
* 1 issue → N tests
* 1 user → N issues/tasks

---

# **3. Installation & Lancement**

## **3.1. Backend**

```bash
cd backend
npm install
npm run dev
```

### **Fichier .env à créer :**

```
DB_HOST=localhost
DB_USER=projet_user
DB_PASS=xxxx
DB_NAME=gestion_projet_db
JWT_SECRET=xxxx
PORT=5000
```

---

## **3.2. Frontend**

```bash
cd frontend
npm install
npm run dev
```

---

# **4. API – Documentation (overview)**

La documentation complète est disponible via Swagger (OpenAPI 3).
URL après lancement backend :

```
/api-docs
```

## **4.1. Endpoints principaux**

### **Auth**

| Methode | Endpoint       | Description     |
| ------- | -------------- | --------------- |
| POST    | /auth/register | Créer un compte |
| POST    | /auth/login    | Connexion JWT   |

### **Users**

| GET | /users/me | Infos utilisateur connecté |

### **Issues**

| GET | /issues | Liste des issues |
| POST | /issues | Créer issue |
| GET | /issues/:id | Détails |
| PUT | /issues/:id | Modifier |
| DELETE | /issues/:id | Supprimer |

### **Tasks**

| POST | /tasks | Créer task |
| PUT | /tasks/:id | Modifier |
| GET | /tasks?issueId= | Lister tasks d’une issue |

### **Releases**

| POST | /releases | Créer une release |
| GET | /releases | Liste |
| PUT | /releases/:id | Modifier |

### **Tests**

| POST | /tests | Créer un test |
| PUT | /tests/:id | Mettre à jour le statut |

### **Docs**

| POST | /docs | Ajouter documentation |
| GET | /docs | Liste |

---

# **5. Documentation Utilisateur**

## **5.1. Connexion & Inscription**

1. Accéder à la page d’accueil
2. Créer un nouveau compte ou se connecter
3. Une fois connecté, accès au dashboard

## **5.2. Navigation principale**

* **Dashboard** : résumé du projet
* **Issues** : gestion des tickets
* **Tasks** : gestion des tâches associées
* **Releases** : versions du projet
* **Tests** : suivi qualité
* **Docs** : documentation du produit

## **5.3. Utilisation des Issues**

* Créer une issue
* Définir type, priorité, statut
* Assigner un membre
* Ajouter des tâches
* Associer à une release

## **5.4. Utilisation des Tâches**

* Créer une task reliée à une issue
* Modifier statut : todo → in_progress → done
* Ajouter estimation et temps passé

## **5.5. Releases**

* Créer une version
* Ajouter issues dans la release
* Marquer comme released

---

# **6. Documentation Administrateur**

L’administrateur dispose de droits élargis :

### **Droits admin**

* Voir tous les utilisateurs
* Gérer les rôles
* Supprimer issues/tâches de n’importe qui
* Gérer la documentation technique interne

### **Modules sensibles**

* Gestion des permissions
* Mise à jour des environnements
* Gestion base de données

---

# **7. Tests & Qualité Logicielle**

## **Backend**

* Jest + Supertest
* Tests d’intégration API

## **Frontend**

* Jest + React Testing Library
* Cypress (E2E)

## **Types de tests**

* Unitaires
* Intégration
* E2E
* Manuels

---

# **8. Sécurité**

* JWT pour authentification
* Mots de passe hashés (bcrypt)
* Validation des entrées (express-validator)
* CORS configuré
* Variables sensibles dans `.env`

---

# **9. Limitations Actuelles**

Selon la release actuelle :

* Pas encore de notifications temps réel
* Intégration Git non activée
* Collaboration en temps réel non incluse
* Vue Kanban en développement

---

# **10. Équipe**

| Nom                 | Rôle                                |
| ------------------- | ----------------------------------- |
| **Saif Amine**      | Full-Stack Developer, Scrum Master  |
| **Ameziane Adnane** | Full-Stack Developer, Frontend Lead |
| **Chelh Monir**     | Full-Stack Developer                |

---

# **11. Maintenance & Évolutions Prévue**

* Vue Kanban
* Notifications
* Intégration GitHub/GitLab
* Export PDF amélioré
* Dashboard avancé

---

# **12. Historique des Versions**

Voir **Release.md** pour les détails des sprints.
