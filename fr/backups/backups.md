# Sauvegardes et restauration

Protéger la progression de votre serveur est crucial. La perte de données peut survenir en raison de mods défectueux, de fichiers de sauvegarde corrompus ou d'erreurs de configuration. Dans ce guide, vous apprendrez à créer des sauvegardes manuelles, à les restaurer et à planifier des sauvegardes automatiques.

---

## 1. Création d'une sauvegarde manuelle

Vous devez toujours créer une sauvegarde avant d'apporter des modifications majeures, de mettre à jour les versions du jeu ou d'ajouter de nouveaux mods.

1. Accédez à votre serveur sur le panneau à l'adresse [panel.vellix.host](https://panel.vellix.host).
2. Cliquez sur l'onglet **"Sauvegardes"** dans le menu de la barre latérale.
3. Cliquez sur le bouton **"Créer une sauvegarde"** dans le coin supérieur droit.
4. Remplissez les champs :
   * **Nom de la sauvegarde :** Donnez à votre sauvegarde un nom descriptif (par exemple, *Avant la mise à jour de Forge* ou *World save 2026*).
   * **Fichiers et dossiers ignorés :** *(Facultatif)* Saisissez les chemins relatifs vers les fichiers ou dossiers que vous souhaitez exclure de la sauvegarde (par exemple, en excluant le dossier `backups/` lui-même ou les journaux volumineux comme `logs/` pour économiser de l'espace). Chaque règle doit aller sur une nouvelle ligne.
5. Cliquez sur **"Démarrer la sauvegarde"**.

Le panneau regroupera vos fichiers dans une archive sécurisée en arrière-plan. La carte de sauvegarde affichera une double flèche jusqu'à ce qu'elle soit complètement terminée.

---

## 2. Restaurer ou télécharger une sauvegarde

Une fois la sauvegarde créée, cliquez sur les trois points `...` sur la carte de sauvegarde pour ouvrir le menu d'action :

* **Restaurer :** rétablit tous les fichiers du serveur dans l'état dans lequel ils se trouvaient au moment de la sauvegarde.
  > [!WARNING] 
  > **La restauration d'une sauvegarde écrasera les fichiers existants.** Vous pouvez cocher la case *"Supprimer les fichiers avant la restauration"* pour nettoyer le répertoire du serveur et vous assurer qu'il ne reste aucun fichier ancien et conflictuel avant de placer les fichiers de sauvegarde.
* **Télécharger :** Télécharge l'archive de sauvegarde (`.tar.gz`) directement sur votre ordinateur.
* **Verrouiller/Déverrouiller :** Le verrouillage d'une sauvegarde empêche sa suppression automatique ou manuelle par erreur lorsque vous atteignez votre limite de sauvegarde.
* **Supprimer :** Supprime définitivement l'archive de sauvegarde pour libérer de l'espace.

---

## 3. Planification des sauvegardes automatiques

La création manuelle de sauvegardes est utile, mais l'automatisation du processus garantit que vous ne perdrez jamais votre progression même si vous oubliez de les exécuter. Vous pouvez configurer une planification de sauvegarde sous l'onglet **"Planifications"** :

1. Cliquez sur l'onglet **"Horaires"** dans la barre latérale.
2. Cliquez sur **"Créer un programme"** en haut à droite.
3. Nommez votre programme (par exemple, *Sauvegarde quotidienne*).
4. Définissez la fréquence en utilisant la notation Cron. Voici les préréglages courants :
   * **Tous les jours à minuit :** Minutes : `0`, Heures : `0`, Jour du mois : `*`, Mois : `*`, Jour de la semaine : `*`
   * **Toutes les 12 heures :** Minutes : `0`, Heures : `*/12`, Jour du mois : `*`, Mois : `*`, Jour de la semaine : `*`
5. Cliquez sur **"Créer un programme"**.
6. Cliquez sur le planning nouvellement créé dans la liste, puis cliquez sur **"Nouvelle tâche"** en haut à droite.
7. Remplacez **Action** par **"Créer une sauvegarde"**.
8. Remplissez les fichiers ignorés (le cas échéant) et cliquez sur **"Créer une tâche"**.

Votre serveur exécutera désormais des sauvegardes automatiques à l'intervalle configuré.