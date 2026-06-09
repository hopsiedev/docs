# Sous-utilisateurs et autorisations

Si vous exécutez un serveur avec une équipe, vous souhaiterez peut-être donner à vos constructeurs, développeurs ou copropriétaires l'accès au tableau de bord du serveur. La fonctionnalité **Sous-utilisateurs** vous permet d'inviter d'autres joueurs à votre panel avec des autorisations spécifiques et granulaires, garantissant qu'ils n'accèdent qu'à ce dont ils ont besoin.

---

## 1. Inviter un sous-utilisateur

Pour ajouter un nouveau sous-utilisateur :

1. Connectez-vous au panneau sur [panel.vellix.host](https://panel.vellix.host) et sélectionnez votre serveur.
2. Cliquez sur l'onglet **"Utilisateurs"** dans le menu de navigation de la barre latérale.
3. Cliquez sur le bouton **"Créer un nouveau"** dans le coin supérieur droit.
4. Remplissez le formulaire d'invitation :
   * **E-mail de l'utilisateur :** Saisissez l'adresse e-mail exacte de la personne que vous souhaitez inviter.
     * *Remarque : s'ils n'ont pas encore de compte sur le panel, ils recevront une invitation par e-mail pour configurer leur mot de passe et s'inscrire.*
   * **Autorisations :** Cochez les cases correspondant aux autorisations que vous souhaitez leur accorder.

---

## 2. Gestion des autorisations granulaires

Vous pouvez personnaliser exactement ce que chaque sous-utilisateur peut faire sur votre serveur. Les autorisations sont divisées en catégories logiques :

### Console de contrôle
* **Contrôler l'état de l'alimentation :** Permet de démarrer, d'arrêter, de redémarrer et de tuer le serveur.
* **Envoyer des commandes :** Permet de saisir et d'envoyer des commandes dans la barre de commandes de la console en direct.

### Gestion des fichiers
* **Lire les fichiers :** Permet d'afficher des répertoires et d'ouvrir des fichiers pour lire le contenu.
* **Écrire des fichiers :** Permet de modifier des fichiers, d'en créer de nouveaux et de télécharger des dossiers.
* **Supprimer les fichiers :** Permet de supprimer des fichiers et des dossiers.
* **Détails SFTP :** Permet d'afficher les détails de la connexion SFTP (ils se connecteront en utilisant leur propre nom d'utilisateur et mot de passe du panneau).

### Bases de données et sauvegardes
* **Créer des bases de données :** Permet de créer et de supprimer des bases de données MySQL.
* **Afficher le mot de passe de la base de données :** Permet de révéler les informations d'identification de connexion à la base de données.
* **Créer des sauvegardes :** Permet d'effectuer des sauvegardes manuelles du serveur.
* **Restaurer les sauvegardes :** Permet de restaurer les fichiers du serveur à l'aide d'une sauvegarde existante.

### Paramètres et horaires
* **Créer des plannings :** Permet de planifier des tâches (redémarrages, sauvegardes, envoi de messages automatiques).
* **Modifier les paramètres de démarrage :** Permet de modifier les variables d'environnement et les options de commande de démarrage.

---

## 3. Révoquer ou modifier l'accès

Vous pouvez modifier les autorisations d'un sous-utilisateur ou supprimer complètement son accès à tout moment :

* **Pour modifier les autorisations :** Accédez à l'onglet **"Utilisateurs"**, cliquez sur l'icône de modification (crayon) à côté de l'adresse e-mail du sous-utilisateur, cochez/décochez les autorisations, puis cliquez sur **"Enregistrer"**.
* **Pour révoquer l'accès :** Cliquez sur l'icône de suppression (poubelle) à côté de l'e-mail du sous-utilisateur. Leur accès au tableau de bord de votre serveur sera immédiatement résilié.