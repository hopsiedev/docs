# Bases de données MySQL

De nombreux plugins et mods de jeu (tels que *LuckPerms*, *CoreProtect*, *Dynmap* ou systèmes d'enregistrement personnalisés) nécessitent une base de données **MySQL/MariaDB** pour stocker les données des joueurs, les autorisations ou bloquer les modifications de manière rapide et fiable, plutôt que de les stocker dans des fichiers plats `.json` ou `.db` locaux, ce qui peut ralentir les performances de votre serveur.

Avec Vellix Hosting, vous pouvez provisionner et gérer des bases de données MySQL en un seul clic directement depuis votre panel Reviactyl.

---

## 1. Création d'une base de données dans le panneau

Pour créer une nouvelle base de données :

1. Accédez au tableau de bord de votre serveur sur le panneau à l'adresse [panel.vellix.host](https://panel.vellix.host).
2. Cliquez sur l'onglet **"Bases de données"** dans le menu de navigation de la barre latérale.
3. Cliquez sur le bouton **"Créer une base de données"** dans le coin supérieur droit.
4. Remplissez les champs :
   * **Nom de la base de données :** fournissez un nom court et descriptif pour la base de données (par exemple, `luckperms` ou `playerdata`).
   * **Connexions depuis :** Définissez ceci sur `%` (signe de pourcentage) pour autoriser les connexions à partir de n'importe quel hôte (il s'agit de la configuration la plus flexible et évite les problèmes de pare-feu en cas de connexion depuis l'extérieur du nœud, par exemple, des serveurs Web ou des proxys BungeeCord).
5. Cliquez sur le bouton **"Créer une base de données"**.

La base de données sera créée instantanément et ajoutée à la liste.

---

## 2. Récupération des informations d'identification de la base de données

Une fois votre base de données créée, vous verrez une carte avec les paramètres de connexion. Cliquez sur l'icône de verrouillage pour révéler le mot de passe :

* **Hôte/Point de terminaison :** L'adresse IP ou le domaine du serveur de base de données (par exemple, `mysql.vellix.host` ou une adresse IP de nœud).
* **Nom de la base de données :** Le nom final généré par le panneau, généralement précédé de votre ID de serveur (par exemple, `s1_luckperms`).
* **Nom d'utilisateur :** Le nom d'utilisateur de la base de données généré automatiquement (par exemple, `u1_xYzA`).
* **Mot de passe :** Le mot de passe unique et sécurisé généré pour cet utilisateur de base de données.
* **Port :** Le port MySQL standard, qui est `3306`.

---

## 3. Configurer votre plugin (Exemple : LuckPerms)

Pour connecter un plugin à votre nouvelle base de données, ouvrez le fichier de configuration du plugin (généralement `config.yml` ou `config.conf`) dans le **Web File Manager** :

1. Recherchez le paramètre `storage-method` ou le type de stockage et remplacez-le de `h2` ou `sqlite` par **`mysql`**.
2. Remplacez les espaces réservés de connexion par vos informations d'identification :

```yaml
# Typical MySQL database connection setup in Minecraft plugins
storage-method: mysql

address: "mysql.vellix.host:3306" # Enter the database Host and Port here
database: "s1_luckperms"          # Enter the generated Database Name
username: "u1_xYzA"               # Enter the Database Username
password: "your_secure_password"  # Enter the revealed Password
```

3. Enregistrez le fichier.
4. Redémarrez votre serveur de jeu depuis la console pour établir la connexion à la base de données.

> [!NOTE] 
> Le provisionnement de la base de données est entièrement gratuit et le stockage de la base de données ne compte pas dans l'allocation de disque de votre serveur principal. Cependant, nous vous conseillons de maintenir l'hygiène de la base de données en purgeant périodiquement les anciens journaux pour garantir des performances de requête optimales.