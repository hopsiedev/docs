---
title: "Hébergement Bot Discord"
sidebarTitle: "Hébergement Bot"
description: "Découvrez comment héberger et créer des serveurs gratuits de bots Discord chez Vellix Hosting"
---

Vellix Hosting propose un hébergement de bot Discord gratuit via l'intégration de notre communauté Discord. Suivez ce guide pour configurer, déployer et gérer votre application Node.js.

---

## Spécifications du Service

Lorsque vous créez un serveur de bot Discord gratuit, vous obtenez :

* **Environnement de Exécution Dédié** : Environnement Node.js isolé dans un conteneur Docker.
* **Mémoire (RAM)** : 250 Mo de mémoire RAM.
* **Stockage** : 1 Go de stockage SSD haute vitesse.
* **Gestion** : Accès console complet et gestion des fichiers FTP/SFTP.

---

## Guide de Démarrage Rapide Étape par Étape

Suivez ces étapes pour déployer votre bot :

### 1. Créez votre Serveur
Rejoignez notre serveur Discord et accédez au canal dédié aux tickets ou à la création de bots :
* **Canal Discord** : [Support Discord](https://discord.com/channels/1504707289385533461/1512867928717000876)
* Cliquez sur le bouton de création de serveur.
* ⚠️ **Important** : Assurez-vous que vos messages privés (DMs) Discord sont ouverts afin que notre bot puisse vous envoyer votre mot de passe temporaire pour le panel !

### 2. Connectez-vous au Panel
* Accédez au panel de contrôle : [panel.vellix.host](https://panel.vellix.host)
* Connectez-vous à l'aide de votre adresse e-mail et du mot de passe temporaire envoyé dans vos DMs Discord.
* (Facultatif) Nous vous recommandons de modifier immédiatement votre mot de passe dans les paramètres de votre compte.

### 3. Transférez les Fichiers de votre Bot
* Sélectionnez votre serveur nouvellement créé dans le tableau de bord.
* Allez dans l'onglet **Gestionnaire de fichiers** dans la barre latérale.
* Transférez les fichiers de votre bot (par exemple, `index.js`, `package.json`, fichiers `.env`).
* > [!CAUTION]
  > **Ne transférez PAS le dossier `node_modules`.** Le panel installera automatiquement les dépendances pour économiser de la bande passante et de l'espace disque.

### 4. Installer les Packages
* Allez dans l'onglet **Console**.
* Vos packages seront installés automatiquement à partir de votre `package.json` lors du premier démarrage du serveur, ou vous pouvez spécifier des options de démarrage personnalisées.

### 5. Démarrez votre Bot
* Configurez vos variables d'environnement, token et secrets sur le panel de contrôle.
* Cliquez sur le bouton vert **Démarrer** dans la Console pour lancer votre bot !
