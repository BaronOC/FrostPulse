# Journal des versions / Changelog

## 1.1 Final — 14 skins intégrés · 17 octobre 2026

Tous les styles sont inclus dans l'installateur Final. Choisissez votre interface dans **Réglages → Style de l'interface** : le changement s'applique immédiatement et votre choix est mémorisé.

| Collection | Styles disponibles |
| --- | --- |
| **FrostPulse** | Moderne · Dot |
| **HOF** | Blanc nacré · Cristal sombre · Polaire |
| **Lightning** | Noir & Or · Carbone · Mesures |
| **KINGPIN** | Copper · Cuivre usiné · Stealth Carbon · XOC Lab |
| **Precision** | Precision X — Classic · Precision X1 — Moderne |

**FrostPulse — Dot** associe noir et graphite, typographie à points, décor PCB monochrome et accents rouges sur les commandes actives. Les autres collections proposent des interfaces claires, cristallines, carbone, cuivre ou inspirées des instruments de monitoring.

### Améliorations et corrections

- **Couleurs personnalisées des tuiles** : le fond choisi est réellement appliqué, avec un contraste adapté des valeurs, titres et minimums/maximums. La disposition propre au skin est conservée.
- **Sélecteur de style plus stable** : réduction du scintillement de la liste, application du style après validation et annulation du choix avec Échap.
- **Fenêtre et redimensionnement** : commandes système intégrées, zones de redimensionnement et marges revues, corrections de découpe de l'ASIC et du pied de fenêtre.
- **Lisibilité** : températures mieux contenues dans les cadres, graduations du cadran Classic adaptées aux petites tailles et champs d'offset plus lisibles.
- **Décors KINGPIN et Precision** : proportions, repeinture après redimensionnement et rendu PCB retravaillés ; Precision X1 Moderne utilise une palette graphite avec détails bleus.
- Les saisies en cours, le run/CSV, les préférences OSD et les profils restent conservés lors d'un changement de style. Les couleurs OSD restent indépendantes de celles de l'interface.

Les fonctions de la Final précédente restent disponibles : **courbes multiples synchronisées dans Mesures, statistiques par run, CSV direct horodaté, SYS, offsets ±15 MHz et lecture ASIC**. Les sondes et contrôles accessibles dépendent du GPU et du pilote.

Version interne **1.1.0.0** ; tag **final-2026-10-17**. [Galerie des skins](docs/SKINS.md).

### English

14 built-in styles across FrostPulse, HOF, Lightning, KINGPIN and Precision, including FrostPulse Dot. Immediate style switching with saved selection; corrected custom tile colors/contrast, reduced selector flicker, integrated window controls and resizing, temperature/dial readability and refined PCB rendering. Inputs, runs/CSV, profiles and OSD preferences are retained. All styles are included in the Final installer; no separate pack is needed. Executable version 1.1.0.0, release tag final-2026-10-17.


## 1.1 Final — Mesures et CSV · 15 octobre 2026

- **History devient Mesures** en français et **Measurements** en anglais.
- **Plusieurs courbes affichées simultanément**, avec un choix mémorisé parmi **19 métriques** : températures, puissance, fréquences, charges, tensions NVVDD/MSVDD, delta et autres mesures disponibles.
- **Temps commun et échelles propres à chaque métrique** pour comparer le comportement du GPU pendant une même session.
- **Lecture synchronisée au survol** et statistiques **minimum / moyenne / maximum** propres à chaque courbe.
- **Agrandir** ouvre une vue plus large, avec retour possible à l'affichage intégré.
- **Démarrer un run / Fermer le run** : un nouveau run remet ses mesures à zéro ; sa fermeture conserve les courbes et statistiques à l'écran tandis que le monitoring principal continue.

### CSV automatique pendant le run

- Le choix du fichier **CSV se fait avant le démarrage**. Annuler conserve le run précédent.
- Les **19 métriques et les sondes mémoire individuelles disponibles** sont enregistrées à chaque relevé, même si elles ne sont pas affichées dans les graphiques.
- Les données sont **écrites et vidées sur disque à chaque relevé**, pour conserver les relevés déjà enregistrés si l'application s'arrête brutalement. Ce comportement a été vérifié sur un processus de test interrompu.
- **Horodatage UTC, date locale avec millisecondes et fuseau, temps écoulé** : les valeurs d'un même relevé partagent le même instant.
- Suivi visible du **nombre de relevés**, de l'heure du dernier relevé et du chemin du fichier.
- Les anciens boutons CSV séparés sont retirés de Mesures : **Démarrer** crée l'enregistrement et **Fermer** clôture le fichier.
- Une erreur d'écriture arrête le run et affiche un état CSV explicite.

Les fonctions de la précédente Final sont conservées, dont SYS, les offsets ±15 MHz et la lecture ASIC. Les mesures disponibles dépendent toujours du GPU et du pilote. Vos profils, couleurs, réglages OSD et préférences sont conservés lors de la mise à jour.

Version interne **1.1.0.0** ; tag daté **final-2026-10-15**. L’ancienne release 1.1 reste disponible.

### English

Redesigned Measurements tab with a saved selection from 19 metrics, synchronized charts and hover readings, individual min/average/max statistics, and expanded view. Starting prompts for the CSV file; closing retains charts and statistics. Every sample is written and flushed to disk, including all metrics and available individual memory sensors, with UTC/local timestamps, milliseconds, time-zone offset and elapsed seconds. Live sample/file status, explicit write errors and simplified CSV controls. Previous Final features and preferences are retained. Executable version remains 1.1.0.0; release tag final-2026-10-15.


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

La lecture ASIC introduite dans la précédente Final reste disponible. Les fonctions SYS dépendent du GPU et du pilote : les données et contrôles non exposés restent indisponibles. La lecture SYS, l'application et la réinitialisation de l'offset ainsi que leur bon fonctionnement ont été vérifiés sur ma RTX 5090 D.

Version interne : **1.1.0.0** · MSI : **1.1.0** · Tag : **v1.1.0**. Mise à jour depuis 1.0 avec conservation des paramètres.

### English

SYS offset, frequency/min/max, history, CSV, profiles and OSD; −15/+15 MHz buttons for all four offsets; customization buttons moved below options; Baron removed from OSD text; About window simplified; GPU-index checks and local service SYS support. Older profiles and preferences are retained. SYS readings, offset application and reset were verified to work correctly on my RTX 5090 D. Executables are version 1.1.0.0, MSI 1.1.0.

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
