<p align="center">
  <img src="assets/frostpulse-banner.svg" alt="FrostPulse by Baron — GPU monitoring and tuning" width="100%">
</p>

<p align="center">
  <a href="https://github.com/BaronOC/FrostPulse/releases/latest"><img src="https://img.shields.io/github/v/release/BaronOC/FrostPulse?label=Final&color=64c7ed" alt="Dernière version Final"></a>
  <img src="https://img.shields.io/badge/Windows-64_bits-2477c5" alt="Windows 64 bits">
  <img src="https://img.shields.io/badge/GPU-NVIDIA-76b900" alt="GPU NVIDIA">
  <img src="https://img.shields.io/badge/Langues-FR_%2F_EN-64c7ed" alt="Français et anglais">
</p>

<p align="center">
  <strong><a href="https://github.com/BaronOC/FrostPulse/releases/latest">Télécharger</a> · <a href="https://discord.gg/ETk7XmNFpB">Discord</a> · <a href="https://github.com/BaronOC/FrostPulse/discussions">Discussions</a> · <a href="https://github.com/BaronOC/FrostPulse/issues/new/choose">Signaler un bug</a> · <a href="README_EN.md">English</a></strong>
</p>

# FrostPulse by Baron

**Monitoring matériel, réglages GPU et suivi en jeu, réunis dans une interface Windows.**

Je développe **FrostPulse** pour les passionnés de matériel qui veulent comprendre le comportement de leur GPU NVIDIA, surveiller ses températures et accéder à ses réglages depuis un seul endroit.

Mon objectif est de construire un outil lisible au quotidien et suffisamment détaillé pour les utilisateurs avancés. Je veux aussi faire grandir une communauté autour du projet : vos configurations, vos retours et vos idées m'aident à décider des prochaines améliorations.

![FrostPulse 1.1 — skin FrostPulse Dot](assets/skin-nothing-dot.png)

*FrostPulse — Dot, l’un des 14 styles intégrés. Capture du logiciel avec données de démonstration ; les sondes et contrôles disponibles dépendent de votre GPU et du pilote.*

## Ce que propose FrostPulse

### Dernière Final — 14 skins intégrés · 17 octobre 2026

J'ai ajouté **14 styles d'interface** dans l'installateur Final : FrostPulse, HOF, Lightning, KINGPIN et Precision. Retrouvez notamment **FrostPulse — Dot**, avec sa typographie à points, son PCB monochrome et ses actions rouges.

Choisissez votre skin dans **Réglages → Style de l'interface** : changement immédiat et choix mémorisé. Les couleurs personnalisées des tuiles sont conservées, avec une meilleure lisibilité ; le redimensionnement et le sélecteur de style ont également été corrigés.

| HOF — Blanc nacré | KINGPIN — Cuivre usiné |
| --- | --- |
| ![HOF Blanc nacré](assets/skin-hof-white.png) | ![KINGPIN Cuivre usiné](assets/skin-kingpin-machined.png) |

*[Voir les 14 styles et la galerie](docs/SKINS.md) · [Télécharger la nouvelle Final et lire les changements](https://github.com/BaronOC/FrostPulse/releases/tag/final-2026-10-17). Captures avec données de démonstration.*

### Mesures et CSV — 15 octobre 2026

J'ai revu l'onglet **Mesures** pour afficher plusieurs courbes synchronisées, choisir parmi **19 métriques** et analyser chaque run avec ses **minimums, moyennes et maximums**. Le bouton **Agrandir** ouvre une vue plus large.

**Démarrer un run** propose le fichier CSV avant la capture et enregistre les relevés directement sur disque, avec dates UTC/locales précises et temps écoulé. **Fermer le run** clôture le CSV tout en conservant les courbes et statistiques à l'écran. La sélection des métriques est mémorisée.

Consultez les [notes complètes et le nouvel installateur Final](https://github.com/BaronOC/FrostPulse/releases/tag/final-2026-10-15).

### Évolutions 1.1 du 12 octobre 2026

Je vous propose **FrostPulse 1.1 Final** : offset et monitoring **SYS**, boutons **−15 / +15 MHz** pour Core, Mémoire, XBAR et SYS, et corrections de la personnalisation et de l'OSD.

La fréquence SYS rejoint le tableau de bord, l'historique, les exports CSV, les profils et l'OSD sur les configurations compatibles. Les anciens profils restent lisibles. Retrouvez tous les changements dans les [notes de la version 1.1](https://github.com/BaronOC/FrostPulse/releases/tag/v1.1.0).

### Qualité ASIC — ajout du 10 octobre 2026

FrostPulse affiche désormais la **qualité ASIC du GPU**, en pourcentage sous son nom, avec les détails accessibles par clic, infobulle et copie de l'identification.

Pour cet ajout, je me suis basé sur la lecture présentée par **HWiNFO** et j'ai vérifié la concordance sur ma RTX 5090 D : **43,3 %** dans les deux logiciels. FrostPulse effectue sa propre lecture native ; **HWiNFO n'a pas besoin d'être installé ou lancé**.

La valeur dépend des données exposées par la carte et le pilote. Si elles ne sont pas disponibles, FrostPulse indique « indisponible ». Cet indice ne garantit pas le potentiel d'overclocking ; la concordance matérielle a été vérifiée sur cette RTX 5090 D.

<details>
<summary>Voir la capture de validation de la lecture ASIC</summary>

![Lecture ASIC à 43,3 % dans FrostPulse](assets/frostpulse-asic.png)

*Capture de validation de l'interface : ASIC à 43,3 %. Les autres mesures dépendent des sondes disponibles lors de la capture.*

</details>

| Fonction | Ce que vous retrouvez dans le logiciel |
| --- | --- |
| **Monitoring GPU et CPU** | Températures GPU, hotspot, VRAM et CPU, fréquences, charges, puissance, ventilation et mémoire utilisée, selon les sondes exposées. |
| **Minimums et maximums** | Repères visibles pour suivre l'évolution des valeurs pendant une session. |
| **Qualité ASIC** | Indice lu nativement sur les GPU compatibles, affiché sous le nom de la carte avec détails et copie. Lecture développée en prenant HWiNFO comme référence de comparaison. |
| **Réglages GPU** | Offsets Core, Mémoire, XBAR et SYS avec boutons −15 / +15 MHz, Power Limit, ventilation et Lock 3D sur les configurations compatibles. |
| **Tensions** | Lecture et contrôles NVVDD / MSVDD lorsqu'ils sont disponibles, application explicite et restauration des références initiales. |
| **Vue PCB / VRAM** | Représentation de la mémoire et suivi des modules lorsque la carte expose des températures individuelles. |
| **Historique et CSV** | Courbes multiples synchronisées, statistiques par run et CSV écrit en direct, avec horodatages UTC/local et temps écoulé. |
| **Profils et personnalisation** | 14 styles intégrés, couleurs personnalisées, profils GPU, préférences et configuration des métriques OSD. |
| **OSD en jeu** | Intégration avec RivaTuner Statistics Server pour les jeux et applications 3D compatibles. |
| **Français et anglais** | Choix de la langue dans l'installateur et interface bilingue. |

## Télécharger et installer

1. Ouvrez la [dernière version Final](https://github.com/BaronOC/FrostPulse/releases/latest).
2. Téléchargez **FrostPulse-1.1-Setup.exe** dans la section **Assets**.
3. Lancez l'installateur, choisissez votre langue et suivez les étapes.
4. Ouvrez FrostPulse depuis le menu Démarrer. Le raccourci Bureau est facultatif.

Les profils, couleurs, réglages OSD et préférences sont conservés lors des mises à jour. Pour plus de détails, consultez le [guide d'installation](docs/INSTALLATION.md).

**Version publiée :** 1.1 Final — 14 skins intégrés · **Build :** 17 octobre 2026 · **Plateforme :** Windows 64 bits.

## Compatibilité

FrostPulse est conçu pour les GPU **NVIDIA**, avec un focus sur les **GeForce RTX série 50** et des fonctions prévues pour les séries **40, 30 et 20**.

La disponibilité de chaque sonde et de chaque réglage dépend du modèle, du VBIOS et du pilote. Une carte compatible avec le monitoring ne donne pas nécessairement accès à tous les contrôles avancés. Les températures VRAM individuelles sont affichées lorsqu'elles sont réellement exposées. **RTSS est nécessaire pour l'OSD en jeu.**

Vous pouvez m'aider à documenter la compatibilité en partageant votre modèle exact, votre version de pilote et les fonctions disponibles sur votre configuration.

## Rejoindre le projet

Je souhaite faire de FrostPulse un projet qui évolue avec ses utilisateurs.

- **[Discord](https://discord.gg/ETk7XmNFpB)** : échanger avec la communauté, présenter sa configuration et partager ses retours.
- **[Discussions GitHub](https://github.com/BaronOC/FrostPulse/discussions)** : poser une question, proposer une idée ou partager un retour d'utilisation.
- **[Issues](https://github.com/BaronOC/FrostPulse/issues/new/choose)** : signaler un problème avec les informations nécessaires pour le reproduire.
- **[Releases](https://github.com/BaronOC/FrostPulse/releases)** : retrouver les versions Final et leurs notes de publication.

Si FrostPulse vous plaît, une **étoile sur le dépôt** et un partage auprès d'autres passionnés aident à faire découvrir le projet. Les retours précis, y compris sur ce qui ne fonctionne pas, sont tout aussi utiles.

## Questions fréquentes et suivi

Consultez la [FAQ](docs/FAQ.md), le [journal des versions](CHANGELOG.md) et le [guide des contributions](CONTRIBUTING.md).

Ce dépôt sert à distribuer les versions Final de FrostPulse et à organiser les échanges avec la communauté. Le code source de l'application n'y est pas publié.

## Crédits

FrostPulse by **Baron**. Le monitoring utilise notamment LibreHardwareMonitor ; certaines fonctions s'appuient sur PawnIO. L'OSD s'intègre à RivaTuner Statistics Server. Les marques citées appartiennent à leurs propriétaires respectifs. FrostPulse est un projet indépendant et n'est pas un produit officiel NVIDIA.
