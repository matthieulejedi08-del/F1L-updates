# Publication des mises a jour

Aucune release OTA installable n'est disponible actuellement.

## Deux distributions distinctes

La premiere installation USB utilise une image flash complete publique,
nettoyee des donnees personnelles. Elle configure les partitions et installe
le firmware qui saura verifier les mises a jour.

Une mise a jour Wi-Fi utilise uniquement l'application ESP32 destinee a
l'emplacement inactif. Une image flash complete ne doit jamais servir d'asset OTA.

## Assets d'une future release validee

- `firmware.bin` : application compatible, pas une sauvegarde flash complete.
- `manifest.json` : manifeste signe avec revision, canal et compatibilite.
- `manifest.sig` : signature du manifeste avec la cle de confiance.

Une somme SHA-256 ne remplace pas une signature. Le volant devra verifier
la signature avec sa cle publique embarquee, puis la compatibilite et
l'integrite de l'application avant de modifier l'emplacement actif.
La cle publique fournie par un telechargement ne doit pas devenir une
nouvelle source de confiance.

## Condition de diffusion

Les essais sur le materiel doivent confirmer conservation des reglages et
dashboards, refus des fichiers invalides, fonctionnement des deux emplacements,
interruption du transfert et retour a une application saine apres un echec.
Le controle des droits de redistribution fait aussi partie des conditions.

Le journal de version, la revision du firmware et les resultats des essais
doivent correspondre aux fichiers effectivement publies. Un candidat dormant,
un resultat de simulation ou une archive de recherche ne suffit pas.

## Donnees exclues

Ne jamais publier de cle privee, passphrase, identifiants Wi-Fi, jeton GitHub,
sauvegarde personnelle du volant ou fichier constructeur sans droit de diffusion.
La cle privee chiffree de signature et sa sauvegarde restent chez l'hote.
Aucun secret GitHub n'est necessaire sur les volants qui telechargent les releases publiques.

`project-status.json` est seulement informatif. Il ne remplace ni le manifeste
signe ni les preuves de validation, et n'active aucune fonction du volant.
