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

![Interface de FrostPulse 1.0 sur une RTX 5090 D](assets/frostpulse-interface.jpg)

*Capture de l'interface sur une configuration RTX 5090 D. Les sondes et réglages affichés varient selon la carte et le pilote.*

## Ce que propose FrostPulse

| Fonction | Ce que vous retrouvez dans le logiciel |
| --- | --- |
| **Monitoring GPU et CPU** | Températures GPU, hotspot, VRAM et CPU, fréquences, charges, puissance, ventilation et mémoire utilisée, selon les sondes exposées. |
| **Minimums et maximums** | Repères visibles pour suivre l'évolution des valeurs pendant une session. |
| **Réglages GPU** | Offsets Core, Mémoire et XBAR, Power Limit, ventilation et Lock 3D sur les configurations compatibles. |
| **Tensions** | Lecture et contrôles NVVDD / MSVDD lorsqu'ils sont disponibles, application explicite et restauration des références initiales. |
| **Vue PCB / VRAM** | Représentation de la mémoire et suivi des modules lorsque la carte expose des températures individuelles. |
| **Historique et CSV** | Suivi des mesures et export pour examiner ou partager une session. |
| **Profils et personnalisation** | Profils GPU, couleurs, préférences et configuration des métriques OSD. |
| **OSD en jeu** | Intégration avec RivaTuner Statistics Server pour les jeux et applications 3D compatibles. |
| **Français et anglais** | Choix de la langue dans l'installateur et interface bilingue. |

## Télécharger et installer

1. Ouvrez la [dernière version Final](https://github.com/BaronOC/FrostPulse/releases/latest).
2. Téléchargez **FrostPulse-1.0-Setup.exe** dans la section **Assets**.
3. Lancez l'installateur, choisissez votre langue et suivez les étapes.
4. Ouvrez FrostPulse depuis le menu Démarrer. Le raccourci Bureau est facultatif.

Les profils, couleurs, réglages OSD et préférences sont conservés lors des mises à jour. Pour plus de détails, consultez le [guide d'installation](docs/INSTALLATION.md).

**Version publiée :** 1.0 Final · **Build :** 20 septembre 2026 · **Plateforme :** Windows 64 bits.

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
