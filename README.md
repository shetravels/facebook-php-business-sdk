# Explications

Il s'agit d'un fork du SDK PHP Facebook.
On rajoute la notion de `app_id` sur la gestion des CustomAudience.

Consulter ce commit pour comprendre les modifications : https://github.com/shetravels/facebook-php-business-sdk/commit/35dfd34

Une PR existe mais l'équipe de Facebook ne s'occupe absolument pas de ce projet : https://github.com/facebook/facebook-php-business-sdk/pull/552

# Mise à jour

Prenons l'exemple d'une mise à jour vers la version v16 de l'API.
Il existe un tag pour chaque version : `16.0.1`.

* Récupérer le projet sur votre environnement de développement
  * `git clone git@github.com:shetravels/facebook-php-business-sdk.git`
  * `git fetch`
* Récupérer le projet de Facebook
  * `git remote add facebook git@github.com:facebook/facebook-php-business-sdk.git`
  * `git fetch facebook`
* Vérifier la présence de deux origines : `git remote -v`
* Positionner son projet sur le commit associé au tag `16.0.1`
  * `git checkout 16.0.1`
* Démarrer une nouvelle branche
  * `git checkout -b fix/v16` 
* Appliquer les modifications du commit [35dfd34](https://github.com/shetravels/facebook-php-business-sdk/commit/35dfd34)
  * Soit manuellement depuis votre IDE, nom du commit : `Add  argument on multi-key methods`
  * Soit avec un peu de chance en appliquant le commit `git cherry-pick 35dfd34`
* Vérifier la présence de votre commit juste après le dernier commit de `16.0.1` : `git log`
* Communiquer vos modifications à Github : `git push origin`
* Vous pouvez à présent mettre à jour le `composer.json` du projet [socialtrip](https://github.com/shetravels/socialtrip/blob/master/composer.json).
