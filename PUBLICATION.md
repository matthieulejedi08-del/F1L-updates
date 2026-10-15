# F1L — Informations et précautions

Cette page complète le [guide rapide](README.md). Elle explique les différents fichiers et les limites connues, sans demander de manipulations supplémentaires.

## Quelle version est disponible ?

La version **R2F150**, publiée le **15 octobre 2026**, est disponible sur la [page des téléchargements](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150).

Elle est prévue **uniquement pour les modèles F1L / MVH compatibles, équipés d'un ESP32 avec 16 Mo de mémoire flash**. Il s'agit d'un firmware communautaire **non officiel**.

## Que dois-je télécharger ?

**Pour une première installation avec un ordinateur :**
téléchargez [F1L_PUBLIC_R2F150.zip](https://github.com/matthieulejedi08-del/F1L-updates/releases/download/R2F150/F1L_PUBLIC_R2F150.zip), puis suivez le fichier **INSTALLATION.txt**. Une première installation avec l'image complète peut **effacer les réglages et dashboards personnels**.

**Pour mettre à jour un volant déjà compatible :**
ne téléchargez pas de fichier à installer manuellement. Utilisez la fonction **Rechercher une mise à jour** dans la page Web **MVH Custom** du volant.

**Pour installer un nouveau dashboard :**
utilisez la fonction d'ajout de dashboards. Ce n'est **pas** la fonction de mise à jour du programme.

## À quoi servent les autres fichiers ?

Ces fichiers servent principalement à la procédure d'installation ou aux vérifications techniques :

| Nom du fichier | Utilité |
| --- | --- |
| `INSTALLATION.txt` | Instructions pour la première installation. |
| `F1L_PUBLIC_R2F150_FLASH_COMPLET_16MO.bin` | Image complète destinée à l'installation **USB**, selon le guide. |
| `firmware.bin` | Programme utilisé par les **mises à jour Wi-Fi** ; ne pas le confondre avec l'image USB complète. |
| `manifest.json` et `manifest.sig` | Informations de version et signature permettant au volant de vérifier la mise à jour. |
| `SHA256SUMS.txt` | Liste d'empreintes permettant de contrôler les téléchargements. |

**N'installez pas ces fichiers au hasard.** L'image complète de 16 Mo ne doit **jamais** être envoyée à l'installateur Wi-Fi. Une empreinte seule ne remplace pas la vérification de signature.

## Qu'est-ce qui a été testé ?

Selon les [notes de la version R2F150](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150) :

- Une mise à jour signée a réussi sur un volant de test.
- Le volant a redémarré deux fois correctement.
- Les boutons **SETTING**, **UP/DOWN** et la télémétrie ont fonctionné sur ce volant.
- Deux contrôles de signature ont réussi ensuite depuis GitHub.

**Ce qui reste à savoir :** l'image USB complète, préparée sans données personnelles, a été contrôlée sur ordinateur, mais **pas réinstallée intégralement sur le volant pendant cet essai**. Le retour automatique à l'ancienne version après un problème n'est pas garanti. Les coupures et procédures de récupération doivent être prises en compte avant toute installation.

La page Web peut également afficher au départ un ancien message concernant le Wi-Fi ; lancer **Rechercher une mise à jour** actualise son état.

## Précautions importantes

Vérifiez toujours le modèle, conservez une sauvegarde et prévoyez un moyen de récupération **USB**. Pendant une mise à jour, gardez l'alimentation stable, la connexion Internet active et la télémétrie arrêtée.

Pour les personnes qui republient ces fichiers : ne diffusez ni clés privées, ni identifiants Wi-Fi, ni sauvegardes personnelles, ni composants constructeur sans autorisation. Le code source du firmware n'est pas fourni ici. Les archives automatiques « Source code » de GitHub ne contiennent que les fichiers descriptifs du dépôt.

Le fichier [`project-status.json`](project-status.json) est une information sur le projet : **ce n'est pas un fichier de mise à jour**.
