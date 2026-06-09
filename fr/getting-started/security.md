# Sécurité du compte

La sécurité de votre compte est essentielle pour protéger les fichiers, les configurations et les lecteurs de votre serveur. Dans ce guide, vous apprendrez comment **changer votre mot de passe** et activer l'**authentification à deux facteurs (2FA)**.

---

## Changer votre mot de passe

Pour des raisons de sécurité, nous vous recommandons fortement de modifier dès que possible le mot de passe temporaire généré automatiquement que vous avez reçu dans votre e-mail de bienvenue.

### Étapes pour mettre à jour votre mot de passe :
1. Connectez-vous au panneau sur [panel.vellix.host] (https://panel.vellix.host).
2. Cliquez sur l'avatar de votre profil dans le coin supérieur droit (ou sur l'icône des paramètres du compte dans la barre latérale).
3. Sélectionnez **"Paramètres du compte"**.
4. Faites défiler jusqu'à la section **"Modifier le mot de passe"**.
5. Entrez votre mot de passe actuel (le mot de passe temporaire de votre e-mail).
6. Saisissez votre nouveau mot de passe et confirmez-le dans le champ ci-dessous.
   * *Conseil : utilisez un mélange de majuscules, de minuscules, de chiffres et de symboles spéciaux.*
7. Cliquez sur le bouton **"Mettre à jour le mot de passe"**.

> [!NOTE] 
> Changer votre mot de passe déconnectera toutes les autres sessions actives pour des raisons de sécurité. Vous devrez utiliser votre nouveau mot de passe pour toute connexion future, ainsi que pour votre connexion SFTP.

---

## Authentification à deux facteurs (2FA)

L'authentification à deux facteurs ajoute une couche de sécurité supplémentaire. Chaque fois que vous vous connectez, vous serez invité à saisir votre nom d'utilisateur, votre mot de passe et un code de vérification dynamique à 6 chiffres généré par une application sur votre téléphone.

### Étapes pour activer 2FA :
1. Accédez à **"Paramètres du compte"**.
2. Localisez la section **« Authentification à deux facteurs »**.
3. Cliquez sur le bouton **"Activer"**.
4. Vous verrez un **QR Code** et une clé de récupération de sauvegarde.
5. Ouvrez une application d'authentification sur votre téléphone (telle que **Google Authenticator**, **Authy** ou **Microsoft Authenticator**).
6. Scannez le code QR à l'aide de votre application.
7. L'application générera un code à 6 chiffres qui change toutes les 30 secondes.
8. Entrez le code actuel à 6 chiffres sur le panneau pour confirmer.
9. Cliquez sur **"Soumettre"** ou **"Activer"**.

> [!IMPORTANT] 
> **Stockez vos clés de récupération dans un endroit sûr et hors ligne.** Si vous perdez votre téléphone ou supprimez l'application, vous aurez besoin des clés de récupération pour vous connecter. Sans elles, vous devrez ouvrir un ticket d'assistance sur notre serveur Discord et notre équipe devra vérifier manuellement votre identité avant de désactiver 2FA.

---

## Réinitialiser un mot de passe oublié

Si jamais vous oubliez votre mot de passe :
1. Visitez [panel.vellix.host](https://panel.vellix.host).
2. Cliquez sur **"Mot de passe oublié ?"** sur la carte de connexion.
3. Entrez l'adresse e-mail de votre compte et cliquez sur **"Envoyer le lien de réinitialisation du mot de passe"**.
4. Suivez le lien envoyé à votre email pour configurer un nouveau mot de passe.