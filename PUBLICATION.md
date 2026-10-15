# F1L — Guide et informations utiles

[← Retour à la page d'accueil](README.md)

## Version disponible

**R2F150** — [Accéder aux téléchargements](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150)

Ce programme communautaire **non officiel** est destiné aux modèles F1L / MVH compatibles, équipés d'un ESP32 avec **16 Mo de mémoire flash**.

## Comment installer ?

**Première installation :** téléchargez le [pack complet](https://github.com/matthieulejedi08-del/F1L-updates/releases/download/R2F150/F1L_PUBLIC_R2F150.zip) et suivez **INSTALLATION.txt** avec un ordinateur et un câble USB. Cette méthode efface les réglages et dashboards personnels présents sur le volant : **sauvegardez-les au préalable**.

**Mise à jour suivante :** sur un volant qui dispose déjà de la fonction de mise à jour Wi-Fi, ouvrez sa page Web, puis **MVH Custom → Rechercher une mise à jour**.

**Nouveau dashboard :** utilisez la fonction dédiée à l'installation des dashboards, et non celle de mise à jour du programme.

## Les fichiers du téléchargement

| Fichier | À quoi sert-il ? |
| --- | --- |
| `F1L_PUBLIC_R2F150.zip` | Pack à utiliser pour la première installation. |
| `INSTALLATION.txt` | Guide à suivre avant de brancher le volant. |
| `F1L_PUBLIC_R2F150_FLASH_COMPLET_16MO.bin` | Image complète pour l'installation USB uniquement. |
| `firmware.bin` | Fichier du programme pour les mises à jour Wi-Fi compatibles. |
| `manifest.json`, `manifest.sig`, `SHA256SUMS.txt` | Fichiers de vérification associés à la version. |

**Ne confondez pas** le fichier USB complet de 16 Mo et `firmware.bin`. N'utilisez pas l'option « Ajouter un dashboard » pour installer l'un de ces fichiers.

## Quelques précautions

Vérifiez la compatibilité du matériel et conservez une sauvegarde ainsi qu'un moyen de récupération par USB. Pendant une mise à jour Wi-Fi, laissez le volant alimenté, connecté à Internet et sans télémétrie active. Un dépannage par USB peut être nécessaire en cas de problème.

Les fichiers publiés ne doivent contenir ni données personnelles, ni mots de passe, ni clés privées. Les composants tiers restent soumis à leurs droits de redistribution.

Le fichier `project-status.json` du dépôt est fourni **à titre d'information uniquement** et ne doit pas être utilisé pour mettre à jour le volant.
