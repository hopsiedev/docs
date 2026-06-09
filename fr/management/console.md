# Console et commandes d'alimentation

La **Console** est l'interface principale pour interagir directement avec votre serveur de jeu. Dans ce guide, vous apprendrez à surveiller l'utilisation du matériel, à envoyer des commandes de jeu et à gérer les états d'alimentation de votre serveur.

---

## Commandes d'alimentation (boutons d'action)

Dans le coin supérieur droit ou dans la barre latérale du tableau de bord de la console, vous trouverez quatre boutons principaux de contrôle de l'alimentation :

* **Démarrer :** Allume le conteneur du serveur et lance le processus de jeu. Utilisez-le si votre serveur est actuellement "Hors ligne".
* **Stop :** Envoie un signal d'arrêt progressif au jeu (par exemple, en exécutant `/stop` ou `/save-all` dans Minecraft). Cela enregistre votre progression et arrête le serveur en toute sécurité.
* **Redémarrer :** Arrête gracieusement le jeu et redémarre-le immédiatement. Idéal pour appliquer des modifications de configuration ou vider le cache RAM.
* **Kill :** Termine instantanément le processus de jeu sans enregistrer.
  > [!CAUTION] 
  > **Utilisez "Kill" uniquement si votre serveur est complètement gelé ou ne répond pas à la commande "Stop".** L'utilisation régulière de Kill peut provoquer une corruption de fichiers, annuler votre progression dans le monde ou corrompre des entrées de base de données.

---

## Graphiques de surveillance en temps réel

Le panneau Reviactyl affiche des graphiques continus en temps réel représentant l'utilisation des ressources de votre serveur :

1. **Utilisation du processeur :** Pourcentage de puissance de traitement utilisée. S'il reste proche de 100 % pendant de longues périodes, les joueurs peuvent rencontrer un décalage (pensez à optimiser les plugins, les mods ou à mettre à niveau votre plan).
2. **Utilisation de la mémoire (RAM) :** Affiche la mémoire actuellement allouée par rapport à la limite de votre plan (par exemple, `4 GB / 8 GB`). 
   * *Si le serveur dépasse sa limite de mémoire, le tueur MOO (Out Of Memory) intégré au panneau arrêtera automatiquement le serveur pour protéger la stabilité du nœud. Optimisez vos fichiers de jeu ou mettez à niveau votre forfait si vous atteignez fréquemment cette limite.*
3. **Utilisation du disque :** Espace de stockage total consommé par vos fichiers de jeu (mods, mondes, journaux, sauvegardes). Assurez-vous de supprimer les anciens fichiers journaux (`latest.log`, `debug.log`) ou les anciennes sauvegardes pour libérer de l'espace disque.

---

## Envoi de commandes de console

Sous l'écran noir du terminal, se trouve une barre de commande de texte intitulée **"Tapez une commande..."** :

* Vous pouvez taper n'importe quelle commande ici pour contrôler le jeu directement depuis la console sans avoir besoin des privilèges d'administrateur du jeu.
* **Ne préfixez pas les commandes avec une barre oblique (`/`)**. Par exemple, tapez `op PlayerName` ou `say Hello World` et appuyez sur Entrée.
* Toutes les réponses ou erreurs du serveur de jeu seront imprimées en temps réel sur le journal de la console ci-dessus.