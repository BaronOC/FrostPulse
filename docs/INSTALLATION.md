# Installation de FrostPulse

## Télécharger

Ouvrez la [dernière release Final](https://github.com/BaronOC/FrostPulse/releases/latest) et téléchargez **FrostPulse-1.1-Setup.exe** dans **Assets**. Ce fichier est l'installateur Windows 64 bits de la version Final.

## Installer

1. Lancez le Setup.
2. Choisissez **English** ou **Français**.
3. Suivez les étapes et la demande d'élévation Windows lorsqu'elle apparaît.
4. Choisissez si vous souhaitez un raccourci sur le Bureau ; il est facultatif et décoché par défaut.
5. Lancez FrostPulse depuis le menu Démarrer.

L'application s'installe dans Program Files et apparaît dans les applications installées de Windows.

## Skins inclus

Les 14 styles sont fournis dans l’installateur. Ouvrez **Réglages → Style de l’interface** pour changer immédiatement de skin et mémoriser votre choix. Aucun pack séparé à installer. Consultez la [galerie des skins](SKINS.md).

## Premier lancement

Vérifiez le GPU sélectionné et les mesures affichées. Les valeurs disponibles dépendent de votre matériel et de votre pilote. Vous pouvez personnaliser les couleurs, les préférences et l'OSD, puis enregistrer un profil adapté à votre configuration.

Pour afficher les métriques en jeu, RTSS doit être installé et actif. Sa présence ne garantit pas que chaque jeu autorise ou affiche l'overlay.

## Mettre à jour

Fermez complètement FrostPulse, puis lancez le nouvel installateur Final 1.1. La mise à jour reconnaît la version 1.0 déjà installée. Les profils, couleurs, réglages OSD et préférences sont conservés lors des mises à jour.

## Désinstaller

Utilisez les applications installées de Windows. L'option de suppression des données personnelles est décochée par défaut, ce qui permet de conserver les préférences pour une réinstallation. Les exports CSV personnels et PawnIO sont conservés.

## Vérifier le fichier

L'empreinte SHA-256 permet de comparer votre téléchargement au fichier publié. Pour la version 1.1 Final du **17 octobre 2026**, avec les 14 skins intégrés :

```text
e425c5895b7fa7a7972b198a29a784fb5e1217425996035fb771ef8caf6306ed
```

Dans PowerShell, depuis le dossier contenant le téléchargement :

```powershell
Get-FileHash -LiteralPath '.\FrostPulse-1.1-Setup.exe' -Algorithm SHA256
```

Si vous rencontrez un problème, consultez la [FAQ](FAQ.md) ou ouvrez un [rapport de bug](https://github.com/BaronOC/FrostPulse/issues/new/choose).
