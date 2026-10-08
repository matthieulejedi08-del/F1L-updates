# F1L-updates

Preparation des mises a jour Wi-Fi F1L pour le volant ESP32 compatible.

## Etat actuel

**Aucune version OTA installable n'est disponible.**

Le mecanisme de mise a jour est en cours d'integration et de validation.
Les archives de preparation et les tests sur ordinateur ne constituent pas
un firmware a flasher. Ne pas les envoyer via **Add dashboard**.

## Fonctionnement prevu

Une premiere installation USB du firmware compatible OTA sera necessaire.
Ensuite, la page web du volant proposera une recherche de mise a jour,
les changements de version et une confirmation avant installation.

Le volant devra etre connecte a un reseau avec acces Internet. Aucun compte
GitHub ni mot de passe GitHub ne devra etre configure sur le volant pour
telecharger les versions publiques.

Les reglages et dashboards devront etre conserves. La nouvelle application
sera ecrite dans l'emplacement inactif, apres verification de compatibilite,
signature et integrite. Le retour automatique en cas d'echec de demarrage
devra etre teste sur le materiel avant diffusion.

## Deux installations distinctes

- **Add dashboard** installe les fichiers d'un dashboard compatible.
- **Mise a jour firmware** installera l'application du volant.

Une image USB complete ne devra jamais etre envoyee a l'installateur OTA.
Les boutons, fichiers autorises et commandes exactes seront documentes
avec la premiere version effectivement validee.

## Conditions avant publication

- Verification de la signature et refus des fichiers modifies ou incompatibles.
- Essais sur les deux emplacements d'application.
- Essais de coupures reseau et alimentation, puis de retour a une version saine.
- Verification de la conservation des reglages et dashboards.
- Controle des droits de redistribution du firmware et des ressources.
- Absence de donnees personnelles, sauvegardes privees et cles privees.

La cle publique de verification sera embarquee dans le firmware de confiance.
La cle privee de signature ne sera jamais publiee dans ce depot.

Les releases seront ajoutees uniquement apres ces validations. Il n'y a
actuellement aucun lien de telechargement de mise a jour a utiliser.
