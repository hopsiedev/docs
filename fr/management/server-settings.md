# Options de démarrage et allocations de ports

Pour exécuter des mods personnalisés, configurer des systèmes de vote, configurer des chats vocaux ou modifier la version de Java exécutée par votre serveur, vous devrez gérer vos allocations de ports et vos variables de démarrage.

---

## 1. Allocations de ports (paramètres réseau)

Votre serveur se voit attribuer une adresse IP et un port principaux (par exemple, `190.22.44.112:25565`). Certains plugins (tels que *Dynmap*, *Votifier* ou *Simple Voice Chat*) nécessitent leurs propres ports supplémentaires pour communiquer.

### Comment demander et attribuer des ports supplémentaires :
1. Connectez-vous à [panel.vellix.host](https://panel.vellix.host) et sélectionnez votre serveur.
2. Cliquez sur l'onglet **"Réseau"** dans le menu de la barre latérale.
3. Si vous disposez d'allocations disponibles, cliquez sur **"Créer une allocation"** (ou ouvrez un ticket d'assistance sur Discord si vous avez besoin de ports supplémentaires attribués à votre nœud).
4. Le nouveau port apparaîtra dans la liste.
5. Dans le fichier de configuration de votre plugin, remplacez le port par défaut par votre nouveau port attribué (n'utilisez jamais de ports aléatoires ; utilisez uniquement les ports spécifiquement alloués à votre serveur dans l'onglet Réseau).

---

## 2. Modification des options de démarrage

L'onglet **"Démarrage"** contient des variables d'environnement clés qui déterminent la manière dont l'exécutable du serveur de jeu est lancé :

* **Version Java :** Sélectionnez la version du kit de développement Java (JDK).
  * **Java 8/11 :** Pour les anciennes versions de Minecraft (1.12.2 et inférieures).
  * **Java 17 :** Standard pour Minecraft 1.18 à 1.20.4.
  * **Java 21 :** Standard pour Minecraft 1.20.5 et supérieur.
* **Fichier Jar du serveur :** Le nom du fichier que le serveur exécutera (par exemple, `server.jar` ou `vanilla.jar`). Assurez-vous que le fichier téléchargé dans votre gestionnaire de fichiers porte exactement le même nom que celui saisi ici.
* **Variables de commande de démarrage :** Indicateurs personnalisés tels que le nombre maximum de joueurs, les ports de requête ou les versions du serveur en fonction du jeu.

> [!IMPORTANT] 
> Certaines variables de démarrage sont verrouillées par le système pour maintenir la stabilité. Si vous devez apporter des modifications aux champs verrouillés ou si vous avez besoin d'indicateurs de démarrage personnalisés (tels que les indicateurs d'Aikar pour les performances), contactez notre équipe d'assistance sur Discord.