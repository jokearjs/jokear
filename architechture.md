# Jōkkær

**Jōkkær** est une plateforme de messagerie open source conçue pour offrir une alternative puissante et flexible à Slack. L'architecture du projet est basée sur une API REST écrite en NestJS, qui communique avec les clients via des requêtes HTTP. La plateforme utilise également WebRTC pour la communication en temps réel, permettant des fonctionnalités telles que les appels vidéo et la messagerie instantanée.

## Architecture Globale du Projet Jōkkær

### Vue d'ensemble

L'architecture de Jōkkær est conçue pour être modulaire et extensible. Elle comprend plusieurs composants clés :

1. **API REST (NestJS)**
   - **Description**: L'API REST est le cœur du projet, développée avec NestJS. Elle expose les endpoints nécessaires pour interagir avec la plateforme, gérer les utilisateurs, les canaux, les messages et les fichiers.
   - **Responsabilités**:
     - Authentification et autorisation
     - Gestion des utilisateurs et des équipes
     - Gestion des canaux de discussion et des messages
     - Gestion des fichiers et des pièces jointes
     - Intégrations avec des services tiers

2. **Base de Données**
   - **Description**: La base de données stocke toutes les informations nécessaires à la gestion de la plateforme, y compris les utilisateurs, les messages, les canaux et les fichiers.
   - **Type**: PostgreSQL (ou tout autre système de gestion de base de données relationnelle)
   - **Responsabilités**:
     - Stockage et récupération des données
     - Gestion des relations entre les entités (utilisateurs, messages, canaux)

3. **Clients**
   - **Description**: Les clients interagissent avec l'API REST pour accéder aux fonctionnalités de la plateforme. Ils peuvent être des applications web, des applications mobiles ou des clients de bureau.
   - **Technologies**:
     - **Application Web**: Développée avec des frameworks modernes comme Vue.js, React, ou Angular.
     - **Application Mobile**: Développée avec des technologies comme React Native ou Flutter.
     - **Application de Bureau**: Développée avec des technologies comme Electron.

4. **Serveur de Communication (WebRTC)**
   - **Description**: Ce composant gère les communications en temps réel, telles que les appels vidéo et les messages instantanés, en utilisant WebRTC.
   - **Technologie**: WebRTC
   - **Responsabilités**:
     - Gestion des connexions en temps réel pour les appels vidéo et la messagerie instantanée
     - Échange de données multimédia (audio, vidéo, texte) en temps réel
     - Signalisation pour établir et maintenir les connexions WebRTC

5. **Services et Intégrations**
   - **Description**: Services externes et intégrations permettent d'étendre les fonctionnalités de la plateforme.
   - **Exemples**:
     - Intégrations avec des outils de productivité (calendriers, gestionnaires de tâches)
     - Services de stockage de fichiers externes
     - Services de notification

### Flux de Communication

- **Client vers API REST**: Les clients envoient des requêtes HTTP (GET, POST, PUT, DELETE) à l'API REST pour interagir avec la plateforme.
- **API REST vers Base de Données**: L'API REST communique avec la base de données pour stocker et récupérer les données nécessaires.
- **Client vers Serveur de Communication (WebRTC)**: Pour les fonctionnalités en temps réel, les clients établissent des connexions WebRTC pour la messagerie instantanée et les appels vidéo.
- **API REST vers Services Externes**: Pour les intégrations et les services externes, l'API REST envoie des requêtes aux services tiers via des API externes.

### Diagramme d'Architecture

*soon*

### Conclusion

L'architecture de Jōkkær est conçue pour être modulaire et extensible, permettant une gestion efficace des utilisateurs, des messages et des canaux tout en offrant une communication en temps réel via WebRTC. Cette structure permet une intégration facile avec des services tiers et une personnalisation selon les besoins des utilisateurs.

