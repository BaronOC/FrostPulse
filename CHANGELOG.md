# Journal des versions / Changelog

## 1.1 Final · 12 octobre 2026

- **SYS OFFSET** rejoint les offsets Core, Mémoire et XBAR sur les GPU compatibles. Il est pris en compte par les commandes Appliquer et Réinitialiser.
- **Monitoring SYS** : fréquence, minimum et maximum dans le tableau de bord, suivi dans l'historique, export CSV et affichage dans l'OSD.
- **Profils avec SYS** : la nouvelle valeur peut être enregistrée ; les anciens profils restent lisibles et se chargent avec SYS à zéro. Charger un profil n'applique pas automatiquement ses réglages.
- **Boutons −15 / +15 MHz** pour les quatre offsets, en remplacement des petits curseurs. La saisie directe et la validation par Entrée ou Appliquer restent disponibles. Un clic prépare la valeur ; il ne l'applique pas immédiatement au GPU.

### Corrections et améliorations

- Les boutons **Appliquer / Annuler** de la personnalisation sont désormais placés sous les options, sans chevauchement lorsque la liste de métriques s'allonge.
- La mention **« By Baron »** est retirée des textes OSD, y compris du mode Benchmark et de l'affichage personnalisé. L'option de titre est renommée **« Titre FrostPulse »** ; les préférences existantes sont conservées.
- La fenêtre **À propos** est simplifiée avec le retrait du bouton « PCI database / license ». Les catalogues d'identification et les notices embarquées sont conservés.
- Le monitoring reste associé au GPU NVIDIA sélectionné ; les indices de GPU hors plage sont refusés.
- Le service local prend en charge SYS tout en conservant la compatibilité avec ses anciens clients.
- L'application, l'installateur et la version affichée dans Windows passent à **1.1**.

La lecture ASIC introduite dans la précédente Final reste disponible. Les fonctions SYS dépendent du GPU et du pilote : les données et contrôles non exposés restent indisponibles. La lecture SYS a été vérifiée sur ma RTX 5090 D ; l'application et la réinitialisation SYS sur le matériel n'ont pas été exécutées pendant les vérifications de développement.

Version interne : **1.1.0.0** · MSI : **1.1.0** · Tag : **v1.1.0**. Mise à jour depuis 1.0 avec conservation des paramètres.

### English

SYS offset, frequency/min/max, history, CSV, profiles and OSD; −15/+15 MHz buttons for all four offsets; customization buttons moved below options; Baron removed from OSD text; About window simplified; GPU-index checks and local service SYS support. Older profiles and preferences are retained. SYS readings checked on my RTX 5090 D; hardware SYS Apply/Reset not performed during development verification. Executables are version 1.1.0.0, MSI 1.1.0.

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
