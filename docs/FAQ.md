# Questions fréquentes

## Qu'est-ce que FrostPulse ?

FrostPulse by Baron est un logiciel Windows de monitoring matériel et de réglage des GPU NVIDIA. Il regroupe les mesures, les réglages disponibles, les profils, la vue mémoire et la configuration de l'OSD.

## Où télécharger la version officielle ?

Dans les [Releases de ce dépôt](https://github.com/BaronOC/FrostPulse/releases/latest), sous **Assets**. Téléchargez le fichier Setup de la version Final.

## Pourquoi ma carte n'affiche-t-elle pas toutes les mesures ?

Les sondes exposées varient selon la carte et le pilote. La température de jonction VRAM et les températures individuelles des modules sont deux informations différentes : la présence de l'une ne garantit pas l'accès aux autres.

## Tous les réglages fonctionnent-ils sur toutes les RTX ?

Non. Les possibilités dépendent du modèle, du VBIOS et du pilote. Un réglage avancé peut être indisponible même si le monitoring fonctionne. Partagez votre configuration dans les Discussions pour aider à documenter les différences.

## Faut-il RTSS pour l'overlay ?

Oui, l'OSD en jeu s'appuie sur RivaTuner Statistics Server. Vérifiez que RTSS est installé et actif, et que le jeu ou l'application 3D est compatible avec son overlay.

## Les profils sont-ils conservés lors d'une mise à jour ?

Oui, les profils, couleurs, réglages OSD et préférences sont conservés lors des mises à jour. À la désinstallation, la suppression des données personnelles est une option décochée par défaut.

## Où signaler un problème ?

Utilisez les [Issues](https://github.com/BaronOC/FrostPulse/issues/new/choose) et indiquez votre version de FrostPulse, votre GPU, votre version de Windows, votre pilote et les étapes pour reproduire le problème. Pour une question ou un échange, préférez les Discussions ou le Discord.

## Le code source est-il disponible ?

Ce dépôt distribue les versions Final et leur documentation. Le code source de l'application n'est pas publié ici.

## Puis-je contribuer sans écrire de code ?

Oui. Des rapports de bug précis, des retours de compatibilité, des suggestions expliquées, des corrections de documentation et le partage du projet aident directement à faire évoluer FrostPulse.
