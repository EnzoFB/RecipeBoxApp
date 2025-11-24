# RecipeBox App 📋

Une application de gestion de recettes et d'ingrédients desktop moderne, construite avec **Electron Forge** et **SQLite3**.

## 🎯 Fonctionnalités

- ✨ **Gestion des recettes** : Créer, modifier, supprimer et consulter vos recettes préférées
- 🥘 **Gestion des ingrédients** : Organiser et gérer vos ingrédients avec leurs propriétés
- 🔍 **Recherche et filtrage** : Trouvez rapidement vos recettes par nom, catégorie ou ingrédient
- 📊 **Base de données locale** : Données stockées localement avec SQLite3 pour une performance optimale
- 🎨 **Interface intuitive** : Application de bureau responsive et facile d'utilisation

## 🛠️ Stack Technologique

- **Framework** : [Electron](https://www.electronjs.org/) - Créer des applications desktop multi-plateforme
- **Build Tool** : [Electron Forge](https://www.electronforge.io/) - Workflow moderne pour Electron
- **Database** : [SQLite3](https://www.sqlite.org/) - Base de données embarquée fiable et performante
- **Langage** : [TypeScript](https://www.typescriptlang.org/) - JavaScript typé pour une meilleure expérience développeur
- **Runtime** : Node.js

## 📋 Prérequis

- Node.js (v14 ou supérieur)
- npm ou yarn
- Git

## 🚀 Installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/EnzoFB/RecipeBoxApp.git
cd RecipeBoxApp
```

### 2. Installer les dépendances

```bash
npm install
```

### 3. Lancer l'application en développement

```bash
npm start
```

## 📦 Scripts disponibles

```bash
# Lancer l'application en mode développement
npm start

# Lancer ESLint pour vérifier le code
npm run lint

# Construire l'application packagée
npm run package

# Générer les installeurs pour différentes plateformes
npm run make

# Publier l'application (requiert configuration)
npm run publish
```

## 📁 Structure du projet

```
RecipeBoxApp/
├── src/
│   ├── index.html        # Page HTML principale
│   ├── index.ts          # Point d'entrée du processus principal
│   ├── index.css         # Styles globaux
│   ├── preload.ts        # Script de préchargement pour la sécurité
│   └── renderer.ts       # Code du processus de rendu
├── webpack/
│   ├── webpack.main.config.ts      # Configuration Webpack pour le main process
│   ├── webpack.renderer.config.ts  # Configuration Webpack pour le renderer process
│   ├── webpack.rules.ts            # Règles de chargement des fichiers
│   └── webpack.plugins.ts          # Plugins Webpack
├── forge.config.ts       # Configuration Electron Forge
├── tsconfig.json         # Configuration TypeScript
├── package.json          # Dépendances et scripts du projet
└── README.md             # Ce fichier
```

## 🏗️ Architecture

### Architecture Electron

L'application suit le modèle classique Electron avec deux processus :

- **Main Process** : Gère le cycle de vie de l'application et la création des fenêtres
- **Renderer Process** : Affiche l'interface utilisateur

### Base de données

Les données sont persistées localement avec SQLite3, ce qui offre :
- Zéro infrastructure serveur requise
- Données sauvegardées localement sur le disque
- Accès rapide et fiable aux données

## 🔧 Configuration

### Variables d'environnement

Créez un fichier `.env` à la racine du projet si nécessaire :

```env
# Exemple de configuration
NODE_ENV=development
```

### Configurations importantes

- `forge.config.ts` : Configuration générale de Electron Forge
- `tsconfig.json` : Options de compilation TypeScript
- `webpack.*.config.ts` : Configurations Webpack pour les différents processus

## 🐛 Dépannage

### L'application ne démarre pas

```bash
# Nettoyer et réinstaller les dépendances
rm -r node_modules package-lock.json
npm install
npm start
```

### Erreurs de compilation TypeScript

```bash
# Vérifier la configuration TypeScript
npx tsc --noEmit
```

## 📄 Licence

Ce projet est sous licence **MIT**. Voir le fichier `LICENSE` pour plus de détails.

## 📚 Ressources utiles

- [Documentation Electron](https://www.electronjs.org/docs)
- [Guide Electron Forge](https://www.electronforge.io/guides)
- [Documentation SQLite3 pour Node.js](https://github.com/mapbox/node-sqlite3/wiki)
- [Guide TypeScript](https://www.typescriptlang.org/docs/)