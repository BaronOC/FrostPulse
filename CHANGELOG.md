# Journal des versions / Changelog

## 1.0 Final — mise à jour ASIC · 10 octobre 2026

- Ajout de la qualité ASIC du GPU en pourcentage sous son nom.
- Détails accessibles par clic, infobulle et copie de l'identification ; affichage français / anglais.
- Lecture native des données GPU, sans installation ni exécution de HWiNFO. HWiNFO a servi de référence de comparaison pendant le développement.
- Concordance vérifiée sur la RTX 5090 D : **43,3 %** dans FrostPulse et dans la capture HWiNFO 8.55-6093 utilisée pour la validation.
- Affichage « indisponible » si le GPU ou le pilote n'expose pas les données nécessaires. Aucune valeur d'une autre carte n'est reprise.

Cet indice ne garantit pas le potentiel d'overclocking. La disponibilité sur d'autres GPU et pilotes reste à documenter avec les retours de la communauté.

La version interne des exécutables reste **1.0.0.0**. Cette publication est identifiée séparément par le tag **final-2026-10-10**, sans remplacer la release initiale.

### English

GPU ASIC quality is now displayed below the GPU name, with details accessible through a click, tooltip and identification copy. The reading is native and does not require HWiNFO; HWiNFO was used as a comparison reference during development. Agreement was verified on an RTX 5090 D at **43.3%**. Unsupported GPU/driver readings show as unavailable. This index does not guarantee overclocking potential.

The executable version remains **1.0.0.0**. This update uses the separate **final-2026-10-10** release tag; the original release is retained.

## 1.0 Final

Build du 20 septembre 2026. Première publication de cette version Final sur le dépôt FrostPulse.

- Monitoring GPU / CPU, valeurs minimum et maximum et historique.
- Vue PCB / VRAM et lectures individuelles lorsqu'elles sont exposées par le matériel.
- Réglages GPU disponibles, profils et personnalisation.
- Contrôles de tension avec restauration des références initiales et relecture des valeurs appliquées.
- Identification du GPU croisant les identifiants PCI et les correspondances VBIOS documentées.
- Configuration de l'OSD et intégration RTSS.
- Interface et installateur français / anglais.
- Conservation des profils et préférences lors des mises à jour.
- Désinstallation dédiée avec suppression facultative des données personnelles.

Les fonctions disponibles dépendent du modèle de GPU, du VBIOS et du pilote.

### English

September 20, 2026 build. First publication of this Final version in the FrostPulse repository.

GPU/CPU monitoring, min/max values and history; available PCB/VRAM readings; supported GPU controls, profiles and customization; voltage reference restoration and applied-value readback; PCI/VBIOS-based GPU identification; RTSS OSD integration; French/English application and installer; settings retained during updates; dedicated uninstaller with optional personal-data removal.
