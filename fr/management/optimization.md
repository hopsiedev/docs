# Conseils d'optimisation et de performances du serveur

Le décalage et les élastiques peuvent gâcher l’expérience du joueur. Bien que Vellix Hosting fournisse des processeurs Ryzen 9 haute fréquence et des SSD NVMe rapides, un logiciel serveur non optimisé, des configurations de modules lourdes ou un nombre excessif d'entités peuvent toujours dégrader les performances. 

Suivez ces conseils d'optimisation professionnels pour que votre serveur continue de fonctionner à un bon taux de 20 TPS (Ticks Per Second).

---

## 1. Pré-générez votre monde (critique pour Minecraft)

Générer de nouveaux morceaux à la volée lorsque les joueurs volent avec Elytras ou courent vite est la cause n°1 du décalage du serveur. Il met l'accent à la fois sur les cycles de lecture/écriture du processeur et du disque.

### Comment pré-générer des morceaux :
1. Installez le plugin **Chunky** (compatible avec Spigot, Paper, Fabric, Forge).
2. Arrêtez votre serveur.
3. Dans `server.properties`, définissez la taille de votre frontière mondiale (par exemple, un rayon de 5 000 blocs).
4. Démarrez le serveur et exécutez ces commandes dans la **Console** :
   * `chunky center 0 0` (définit le centre de génération).
   * `chunky radius 5000` (définit le rayon de génération).
   * `chunky start` (démarre le processus de génération).
5. Laissez Chunky terminer la tâche avant de permettre aux joueurs de la rejoindre. Cela peut prendre plusieurs heures selon le rayon. Une fois terminé, le décalage de chargement des morceaux sera pratiquement éliminé.

---

## 2. Optimiser les fichiers de configuration du serveur

Si vous utilisez un serveur Minecraft, utilisez **Paper** ou **Purpur** au lieu de Vanilla ou Spigot. Ils contiennent des correctifs de performances avancés.

Ouvrez les fichiers suivants dans **Web File Manager** et ajustez ces valeurs :

### `server.properties`
* `view-distance=6` (Contrôle le nombre de morceaux envoyés au client. Des valeurs comprises entre 6 et 8 sont recommandées).
* `simulation-distance=4` (Contrôle les entités actives et les ticks qui s'exécutent. Le réduire à 4 ou 5 réduit considérablement la charge du processeur).

### `paper-world-defaults.yml` (ou `spigot.yml`)
* **Plages d'activation des entités :** Réduisez la distance à laquelle les animaux, les monstres et les objets divers se déplacent.
* **Maximum de collisions d'entités :** Limitez le nombre de fois où les entités vérifient les collisions par tick (par exemple, définissez `max-entity-collisions=2`).

---

## 3. Conseils pour la collecte des déchets et la mémoire

* **Utilisez les versions Java modernes :** Les versions Java plus récentes (comme Java 21) disposent d'un garbage collection supérieur (ZGC / G1GC) qui réduit les pics de décalage lors du nettoyage de la mémoire.
* **Évitez les modpacks gonflés :** Chaque mod actif augmente l'empreinte mémoire. Supprimez les mods uniquement esthétiques qui ne sont pas essentiels au gameplay, ou les mods qui effectuent des calculs de ticking excessifs.
* **Surveillez les journaux pour détecter le spam :** Si un plugin génère constamment des erreurs dans votre console, il écrira des milliers de lignes sur votre disque, créant ainsi un décalage de disque. Réparez la configuration ou supprimez le plugin défectueux.