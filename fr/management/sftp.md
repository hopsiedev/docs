# Connexion SFTP (FileZilla / WinSCP)

Pour transférer des dossiers entiers, des cartes lourdes, des modpacks volumineux ou effectuer des modifications groupées sur votre serveur, le gestionnaire de fichiers Web peut être lent. Pour ces tâches, l'utilisation d'un client **SFTP (Secure File Transfer Protocol)** est la meilleure option.

---

## 1. Récupérez vos identifiants SFTP

Chaque serveur de jeu sur Vellix Hosting possède ses propres détails de connexion SFTP uniques :

1. Connectez-vous à votre serveur sur le panneau à l'adresse [panel.vellix.host] (https://panel.vellix.host).
2. Cliquez sur l'onglet **"Paramètres"** ou **"SFTP"** dans le menu de navigation de la barre latérale.
3. Localisez la section **Détails SFTP** pour rechercher :
   * **Adresse du serveur/hôte :** L'adresse du nœud hébergeant votre serveur (par exemple, `sftp.vellix.host` ou une adresse IP).
   * **Port :** Généralement `2022` (le port SFTP standard pour notre démon de panneau).
   * **Nom d'utilisateur :** Un identifiant d'utilisateur unique au format `yourusername.serverid` (par exemple, `admin.a1b2c3d4`).
   * **Mot de passe :** **Il s'agit exactement du même mot de passe** que vous utilisez pour vous connecter au tableau de bord du panneau Web.

---

## 2. Connexion avec FileZilla (recommandé)

[FileZilla](https://filezilla-project.org/) est un client SFTP multiplateforme gratuit disponible pour Windows, macOS et Linux.

### Étapes pour se connecter :
1. Lancez FileZilla.
2. Dans la barre **Quickconnect** en haut, remplissez les champs suivants :
   * **Hôte :** Copiez et collez l'*Adresse du serveur* à partir du panneau.
   * **Nom d'utilisateur :** Copiez et collez le *Nom d'utilisateur* à partir du panneau.
   * **Mot de passe :** Saisissez le mot de passe de votre compte.
   * **Port :** Entrez `2022`.
3. Cliquez sur le bouton **"Connexion rapide"**.
4. Si une invite d'avertissement concernant une *"Clé d'hôte inconnue"* apparaît, cochez la case *"Toujours faire confiance à cet hôte"* et cliquez sur **OK**.
5. Une fois connecté, les fichiers locaux de votre ordinateur s'afficheront à gauche et le répertoire de votre serveur distant apparaîtra à droite. Vous pouvez désormais glisser et déposer des fichiers pour les transférer.

---

## 3. Connexion avec WinSCP (Windows uniquement)

[WinSCP](https://winscp.net/) est un utilitaire Windows uniquement populaire et gratuit pour les transferts sécurisés.

### Étapes pour se connecter :
1. Ouvrez WinSCP.
2. Dans la fenêtre **Connexion**, configurez les éléments suivants :
   * **Protocole de fichier :** Sélectionnez **SFTP**.
   * **Nom d'hôte :** Entrez l'*adresse du serveur* à partir du panneau.
   * **Numéro de port :** Entrez `2022`.
   * **Nom d'utilisateur :** Entrez votre *Nom d'utilisateur* dans le panneau.
   * **Mot de passe :** Saisissez le mot de passe de votre compte.
3. Cliquez sur **"Connexion"** (ou cliquez sur **"Enregistrer"** pour stocker cette session afin d'y accéder plus facilement ultérieurement).
4. Acceptez l'avertissement de clé d'hôte du serveur lors de votre première connexion.

---

## Conseils de transfert essentiels

> [!TIP] 
> **Évitez de transférer des dossiers bruts contenant des milliers de petits fichiers :** Les protocoles comme SFTP nécessitent une poignée de main pour chaque fichier. Transférer directement un dossier contenant 2 000 fichiers mod peut prendre des heures. Au lieu de cela, compressez le dossier sur votre ordinateur, téléchargez le fichier unique `.zip` via SFTP, puis utilisez l'option **"Désarchiver"** du gestionnaire de fichiers Web pour l'extraire en quelques secondes.

> [!WARNING] 
> Si vous mettez à jour le mot de passe de votre compte sur le panneau Web (comme décrit dans le guide de sécurité), votre mot de passe SFTP se met à jour instantanément pour correspondre à celui-ci. N'oubliez pas de mettre à jour vos mots de passe de connexion enregistrés dans FileZilla ou WinSCP !