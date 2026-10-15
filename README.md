# F1L — mises à jour du firmware

Firmware communautaire, **non officiel MVH Studios**, destiné uniquement aux volants F1L/MVH ESP32 **16 Mo compatibles**. Ce dépôt publie les informations et fichiers nécessaires aux mises à jour ; il ne contient **pas** les sources du firmware.

## Dernière version : R2F150

**Publiée le 15 octobre 2026.** [Voir la version R2F150 et ses fichiers](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150).

La publication décrit une installation OTA signée réussie depuis un serveur HTTPS privé, une partition active marquée `VALID`, deux démarrages réussis et deux vérifications de signature depuis GitHub. **L'image USB complète n'a pas été reflashée intégralement pendant cet essai.** Le retour automatique en cas d'échec n'est pas garanti.

## Quelle méthode utiliser ?

| Action | Fichier ou interface | À savoir |
| --- | --- | --- |
| Première installation par USB | `F1L_PUBLIC_R2F150.zip`, puis `INSTALLATION.txt` | L'image complète **16 Mo** remplace également le stockage personnel présent sur le volant : sauvegardez préalablement vos réglages et dashboards. |
| Mise à jour ultérieure par Wi-Fi | Page Web du volant → **MVH Custom** → recherche de mise à jour → confirmation | Nécessite un firmware compatible, une connexion Internet et une alimentation stable. Arrêtez la télémétrie pendant l'opération. |
| Installation d'un dashboard | Fonction d'ajout de dashboard dans **MVH Custom** | Ne pas y envoyer de fichier de firmware. |

**Ne confondez pas** `firmware.bin` (application OTA) et `F1L_PUBLIC_R2F150_FLASH_COMPLET_16MO.bin` (image USB complète). N'envoyez jamais l'image 16 Mo à l'installateur OTA.

## Avant toute installation

- Vérifiez la compatibilité exacte de votre matériel et lisez **`INSTALLATION.txt`** dans la [release](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150).
- Conservez une sauvegarde de vos données et un moyen de récupération par **USB**.
- Ne coupez pas l'alimentation pendant l'installation ; ne lancez pas de télémétrie simultanément.
- N'installez aucun fichier simplement parce qu'il porte le nom `firmware.bin` : utilisez la procédure de mise à jour qui vérifie la signature, la compatibilité et l'intégrité.

## Documentation

- [Publication et contrôles de sécurité](PUBLICATION.md)
- [Statut informatif du projet](project-status.json) — **ce fichier n'est pas un manifeste OTA**.
- [Toutes les versions publiées](https://github.com/matthieulejedi08-del/F1L-updates/releases)

Les archives automatiques **Source code** de GitHub contiennent uniquement les fichiers descriptifs de ce dépôt, pas le code source embarqué.
