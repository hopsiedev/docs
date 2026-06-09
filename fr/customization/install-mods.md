# Téléchargement et installation de mods/plugins

Personnaliser votre serveur avec des mods, des plugins ou des modes de jeu personnalisés est l'un des meilleurs moyens d'améliorer l'expérience de jeu. Ce guide vous guidera dans l'installation de plugins individuels, de mods et de modules de serveur entiers sur votre serveur Vellix Hosting.

---

## 1. Plugins ou mods : qu'est-ce que mon serveur utilise ?

Avant de télécharger des fichiers, vous devez savoir ce que votre logiciel serveur prend en charge :
* **Plugins (Spigot, Paper, Purpur) :** Étendez les fonctionnalités du serveur (comme l'ajout de réclamations, d'économies ou de préfixes de discussion) sans obliger les joueurs à installer quoi que ce soit sur leur ordinateur.
* **Mods (Forge, Fabric, NeoForge) :** Ajoutez des blocs, des objets, des créatures et des dimensions personnalisés. **Le serveur et les joueurs doivent avoir exactement les mêmes mods installés.**

---

## 2. Installation de plugins ou de mods individuels

1. Téléchargez les fichiers `.jar` pour les plugins/mods que vous souhaitez utiliser à partir de sources fiables (par exemple, CurseForge, Modrinth ou SpigotMC).
   * *Assurez-vous qu'ils sont compatibles avec la version du jeu que votre serveur exécute.*
2. Arrêtez votre serveur depuis la **Console**.
3. Ouvrez le **Web File Manager** ou connectez-vous via **SFTP**.
4. Accédez au dossier approprié :
   * Pour les plugins Spigot/Paper/Purpur : Téléchargez les fichiers `.jar` dans le répertoire **`plugins/`**.
   * Pour les mods Forge/Fabric : téléchargez les fichiers `.jar` dans le répertoire **`mods/`**.
5. Revenez à la **Console** et cliquez sur **Démarrer** ou **Redémarrer**.
6. Vérifiez qu'ils ont été correctement chargés :
   * Dans Minecraft, exécutez la commande `plugins` dans la console (ou `/plugins` dans le jeu) pour voir vos plugins actifs.

---

## 3. Installation d'un Modpack complet (par exemple, pack serveur CurseForge)

Pour exécuter un modpack préemballé (comme RLCraft, Pixelmon ou Better MC) :

1. Téléchargez les fichiers **Server Pack** pour le modpack (généralement une archive `.zip` contenant les dossiers `mods`, `config` et les bibliothèques).
2. Arrêtez votre serveur.
3. Ouvrez votre client **SFTP** et connectez-vous au serveur.
4. Si vous disposez de fichiers existants, vous devez d'abord les sauvegarder, puis les supprimer du répertoire du serveur pour éviter les conflits.
5. Téléchargez l'archive modpack `.zip` dans le répertoire racine de votre serveur.
6. Ouvrez le **Web File Manager** dans votre navigateur, localisez le fichier `.zip` téléchargé, cliquez sur les trois points `...` et choisissez **"Désarchiver"** pour extraire tous les fichiers.
7. Vérifiez les paramètres de démarrage :
   * Sous l'onglet **"Démarrage"** dans la barre latérale, assurez-vous d'avoir sélectionné la bonne **version Java** requise par le modpack (par exemple, Java 17 pour Minecraft 1.18+, Java 21 pour Minecraft 1.20.5+).
   * Assurez-vous que le **Fichier Jar du serveur** ou les paramètres de démarrage correspondent aux exigences du script de lancement du modpack.
8. Revenez à la **Console** et cliquez sur **Démarrer**.

---

## Dépannage des problèmes courants

* **Le serveur est bloqué dans une boucle de démarrage :** Vérifiez le journal de la console. Si vous voyez `java.lang.UnsupportedClassVersionError`, cela signifie que votre version de Java est obsolète ou trop récente pour votre version de jeu. Modifiez la version Java dans l'onglet **Démarrage**.
* **Erreur de dépendance manquante :** Certains mods ou plugins nécessitent d'autres mods de la bibliothèque principale pour fonctionner. Lisez la page de description du mod/plugin et téléchargez les dépendances manquantes dans le dossier de votre serveur.
* **Modpack ne charge pas les blocs personnalisés :** Vérifiez que vous avez téléchargé les fichiers mod dans le répertoire `mods/` du serveur et que vous avez installé exactement la même version du modpack sur votre lanceur local (application CurseForge, application Modrinth, Prism Launcher).