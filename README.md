# CalTrack

Journal de calories par repas, scan de codes-barres (Open Food Facts), recettes calculées par part ou au poids, suivi du poids et de l'eau. Interface en français et en anglais.

## Fichiers

| Fichier | Rôle |
|---|---|
| index.html | L'application complète |
| manifest.webmanifest | Permet d'installer l'appli sur l'écran d'accueil |
| sw.js | Fait fonctionner l'appli hors connexion |
| ciqual-2025.js | Les 3 341 aliments courants de la table officielle Ciqual 2025 (Anses), valeurs reprises sans modification |
| icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png | Icônes (Mimi la marmotte) |

## Mettre en ligne sur GitHub Pages

1. Sur github.com, cliquez sur **New repository**. Nom : `caltrack`. Visibilité : **Public**. Cliquez sur **Create repository**.
2. Sur la page du dépôt, cliquez sur **uploading an existing file**.
3. Glissez les 9 fichiers ci-dessus (pas le dossier, les fichiers eux-mêmes), puis cliquez sur **Commit changes**.
4. Allez dans **Settings**, puis **Pages**. Sous **Branch**, choisissez `main` et `/ (root)`, puis **Save**.
5. Attendez une à deux minutes. L'appli est en ligne à l'adresse `https://ninate07.github.io/caltrack/`.

## Installer sur le téléphone

Ouvrez l'adresse dans Chrome, touchez le menu ⋮ puis **Installer l'application** (ou **Ajouter à l'écran d'accueil**). Au premier scan, autorisez l'accès à la caméra.

## Mettre à jour l'appli plus tard

1. Dans le dépôt, cliquez sur `index.html`, puis sur l'icône crayon ou **Add file > Upload files** pour déposer la nouvelle version.
2. Ouvrez `sw.js` et augmentez le numéro dans `caltrack-v11` (v12, puis v13, etc.). Sans ce changement, les téléphones peuvent garder l'ancienne version en mémoire.

## Données

- Vos données restent sur le téléphone, dans le navigateur. Pensez à **Profil > Sauvegarder dans un fichier** régulièrement.
- Les aliments courants viennent de la table Ciqual 2025 : « Anses. 2025. Table de composition nutritionnelle des aliments Ciqual » (Licence Ouverte). Sur les 3 484 aliments de la table, les 143 sans valeur énergétique ne sont pas repris. Une valeur absente de Ciqual (tiret) est signalée dans l'appli, jamais remplacée par une valeur inventée. Les mentions « traces » et « < x » sont affichées telles quelles et comptées 0 dans les totaux.
- Les produits du commerce viennent d'Open Food Facts (licence ODbL), une base collaborative : l'appli signale une fiche dont les calories ne correspondent pas aux macros.
- L'analyse du jour compare vos repas aux repères officiels pour adultes : sel moins de 5 g par jour (OMS, fiche « Réduction de la consommation de sel », 2026), sucres 100 g par jour au maximum hors lactose et galactose (Anses, 2016), fibres au moins 30 g par jour (Anses, 2016), acides gras saturés 12 % des calories au maximum (Anses, 2010).

## Option : laisser Claude Code tout faire

Dans Claude Code, ouvrez le dossier où vous avez décompressé l'archive, puis envoyez ce message :

> Dans ce dossier se trouve mon application CalTrack (9 fichiers). Crée un dépôt GitHub public nommé `caltrack` sur mon compte Ninate07, ajoute tous les fichiers de ce dossier, fais un commit « Première version de CalTrack » et pousse-le sur la branche `main`. Active ensuite GitHub Pages sur la branche `main`, dossier racine. Vérifie que la page https://ninate07.github.io/caltrack/ répond, puis donne-moi l'adresse.
