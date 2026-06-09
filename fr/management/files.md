# Gestionnaire de fichiers Web

Le **Gestionnaire de fichiers** (situé sous l'onglet **Fichiers** dans le menu de la barre latérale) vous permet de gérer toutes les données de votre serveur directement depuis votre navigateur Web sans nécessiter de logiciel externe.

---

## Opérations de base sur les fichiers

Lorsque vous ouvrez le gestionnaire de fichiers, vous verrez le répertoire racine de votre serveur. À partir de là, vous pouvez effectuer plusieurs actions principales :

* **Créer des fichiers et des dossiers :** Cliquez sur les boutons **"Créer un fichier"** ou **"Nouveau dossier"** dans le coin supérieur droit.
* **Modifier les fichiers :** Cliquez sur n'importe quel fichier texte (tel que `.yml`, `.json`, `.conf`, `.properties` ou `.txt`). Cela ouvre un **éditeur de code intégré** avec coloration syntaxique. Après avoir effectué vos modifications, cliquez sur **"Enregistrer le contenu"** en bas.
* **Télécharger des fichiers :** Faites glisser et déposez des fichiers depuis votre ordinateur directement dans la fenêtre du navigateur, ou cliquez sur le bouton **"Télécharger"** pour parcourir et sélectionner les fichiers.
  > [!TIP] 
  > Le gestionnaire de fichiers Web est parfait pour les modifications de configuration individuelles ou le téléchargement de fichiers plus petits (moins de 100 Mo). Pour les transferts plus importants (tels que des cartes entières, des mondes ou de grands modpacks), nous vous recommandons de vous connecter via **SFTP**.

---

## Menu d'action (Les trois points `...`)

À droite de chaque fichier et dossier, vous trouverez un bouton à trois points `...` qui ouvre le menu d'action :

1. **Renommer :** Modifiez le nom d'un fichier ou d'un répertoire.
2. **Déplacer/Copier :** Déplacez le fichier. Vous pouvez déplacer des fichiers en fournissant leur chemin relatif (par exemple, déplacez `server.properties` dans un dossier en saisissant `backup-configs/server.properties`).
3. **Télécharger :** Enregistrez le fichier directement sur votre ordinateur.
4. **Supprimer :** Supprimez définitivement le fichier ou le dossier du stockage du serveur.
   > [!WARNING] 
   > La suppression de fichiers est permanente et irréversible. Créez une sauvegarde de votre serveur avant d'effectuer des suppressions groupées.

---

## Compresser et extraire des archives (.zip)

Télécharger des dossiers contenant des centaines de petits fichiers individuels (tels que des modpacks ou des configurations de plugins) un par un est très inefficace. Au lieu de cela :

1. Compressez le dossier sur votre ordinateur dans une archive `.zip`.
2. Téléchargez le fichier unique `.zip` sur le panneau (via le gestionnaire de fichiers Web ou SFTP).
3. Dans le gestionnaire de fichiers Web, cliquez sur les trois points `...` à côté du fichier `.zip` téléchargé.
4. Sélectionnez **"Désarchiver"** ou **"Décompresser"**. Le panneau extraira instantanément tous les fichiers et sous-dossiers.
5. *(Facultatif)* Supprimez le fichier `.zip` téléchargé pour économiser de l'espace disque.

Vous pouvez également compresser des fichiers sur le panneau en les sélectionnant à l'aide des cases à cocher à gauche, en cliquant sur le bouton **"Archiver"** en haut et en téléchargeant le fichier `.zip` résultant.