**Cahier des Charges pour une Application Angular et Express.js utilisant l’API "Gel des Avoirs"**

---

## 1. Contexte et Objectifs
L’objectif de ce projet est de développer une application web permettant d’interagir avec l’API "Gel des Avoirs" (à partir de https://api.gouv.fr/les-api/api-gels-avoirs). L’application vise à fournir une interface intuitive pour consulter, rechercher et filtrer les informations relatives aux gels d’avoirs en France, en respectant les contraintes légales et techniques.

---

## 2. Spécifications Fonctionnelles

### 2.1 Fonctionnalités Principales
- **Recherche d’avoirs gelés** :
  - Recherche par nom, identifiant ou type d’entité.
  - Filtrage par date, type de gel ou localisation.
  - Affichage paginé des résultats.

- **Visualisation des détails** :
  - Accès à des informations complètes sur une entité (nom, raison du gel, dates).

- **Exportation des données** :
  - Exporter les résultats de recherche sous format PDF ou CSV.

### 2.2 Fonctionnalités Complémentaires
- **Favoris** : Marquer des entités pour un accès rapide ultérieur.
- **Statistiques** : Affichage de statistiques synthétiques sur les gels d’avoirs.

---

## 3. Spécifications Techniques

### 3.1 Frontend
- **Technologie** : Angular.
- **Langage** : TypeScript, HTML, SCSS.
- **Bibliothèques** :
  - Angular Material pour les composants UI.
  - Chart.js pour les visualisations statistiques.

### 3.2 Backend
- **Technologie** : Node.js avec Express.js.
- **Base de Données** : MongoDB.
- **API externe** : Consommation de l’API "Gel des Avoirs" via des requêtes REST.
- **Middleware** :
  - Validation des données avec Joi.
  - Gestion des erreurs avec un middleware centralisé.

### 3.3 Infrastructure
- **Hébergement** : En local uniquement.
- **Sécurité** :
  - Utilisation de certificats HTTPS locaux.
  - Contrôle strict des CORS pour l’accès aux API.

---

## 4. User Stories

### Utilisateur : Anonyme
1. **En tant qu’utilisateur, je veux rechercher des avoirs gelés par nom ou identifiant**
   - Critères d’acceptation :
     - Le système permet de saisir un mot-clé ou un identifiant.
     - Les résultats sont affichés en moins de 2 secondes.

2. **En tant qu’utilisateur, je veux consulter les détails complets d’un avoir gelé**
   - Critères d’acceptation :
     - Les détails incluent toutes les informations disponibles.
     - Une navigation fluide entre les résultats et les détails.

3. **En tant qu’utilisateur, je veux exporter les données au format CSV ou PDF**
   - Critères d’acceptation :
     - L’export génère un fichier contenant les informations visibles.

4. **En tant qu’utilisateur, je veux voir un résumé statistique des gels d’avoirs**
   - Critères d’acceptation :
     - Les statistiques incluent le nombre total de gels et leur répartition par type.

---
