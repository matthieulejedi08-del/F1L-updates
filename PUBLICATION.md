# Publication du firmware F1L

## Version publiée

La release **R2F150** a été publiée le **15 octobre 2026** : [consulter les fichiers et notes de version](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150).

Elle est destinée au matériel F1L/MVH **ESP32 16 Mo compatible** et reste un firmware **communautaire non officiel**.

## Deux formats à ne jamais confondre

| Fichier | Usage |
| --- | --- |
| `F1L_PUBLIC_R2F150_FLASH_COMPLET_16MO.bin` | **Première installation USB** de l'image complète ; remplace aussi les données personnelles présentes dans les 16 Mo. |
| `firmware.bin` | **Application pour OTA**, pas une image flash complète. À utiliser uniquement via le mécanisme de mise à jour compatible et vérifié. |
| `manifest.json` et `manifest.sig` | Manifeste de version et signature associée. |
| `SHA256SUMS.txt` | Empreintes pour contrôler l'intégrité des fichiers téléchargés. |
| `F1L_PUBLIC_R2F150.zip` et `INSTALLATION.txt` | Paquet public et guide de première installation. |

**Important :** une empreinte SHA-256 ne remplace pas une signature. La clé publique doit déjà être intégrée dans le firmware de confiance ; une clé téléchargée en même temps que le manifeste ne devient pas automatiquement fiable. La clé privée de signature n'est pas publiée.

## Validations annoncées pour R2F150

Selon les notes de la [release](https://github.com/matthieulejedi08-del/F1L-updates/releases/tag/R2F150) :

- installation OTA signée réalisée sur le volant de test depuis un serveur HTTPS privé ;
- partition active vérifiée `VALID` et deux redémarrages réussis ;
- commandes **SETTING**, **UP/DOWN** et télémétrie validées sur ce volant ;
- deux vérifications ultérieures des signatures GitHub depuis R2F150.

**Limites connues :** l'image USB publique nettoyée a été assemblée et contrôlée **hors appareil**, sans reflash complet pendant cet essai. Aucun retour arrière automatique n'est garanti ; conserver l'accès USB est indispensable. Une mention initiale « Wi-Fi non activé » peut rester visible avant que le bouton de recherche n'actualise l'état.

## Points de prudence

Avant de diffuser ou installer une nouvelle version, vérifier sur matériel : la compatibilité, la conservation des réglages pour les mises à jour applicatives, le rejet des signatures/fichiers invalides, les interruptions de transfert et la récupération après échec. Vérifier également les droits de redistribution des composants du firmware.

Ne publiez jamais de clé privée, passphrase, identifiant Wi-Fi, jeton GitHub, sauvegarde personnelle ou fichier constructeur sans droit de diffusion. Le dépôt public ne contient pas les sources du firmware.

## Statut du dépôt

Le fichier [`project-status.json`](project-status.json) est **informatif uniquement** : ce n'est ni un manifeste signé, ni un mécanisme permettant au volant d'installer une mise à jour. Pour les instructions d'installation, utilisez les **assets de la release**.
