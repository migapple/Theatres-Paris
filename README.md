# 🎭 Théâtres Paris

**Guide bilingue des théâtres et opéras parisiens**  
iOS app built with Capacitor 6 · HTML / CSS / JS · Leaflet Maps

---

## 📱 Description

Théâtres Paris est un guide de référence bilingue français/anglais répertoriant **39 théâtres et opéras parisiens** avec leurs informations pratiques, leur histoire et leurs spectacles emblématiques.

L'app couvre l'intégralité des grandes scènes parisiennes : du Palais Garnier aux Folies Bergère, de la Comédie-Française au Bataclan, du Théâtre de la Huchette (record mondial Ionesco) aux Bouffes-du-Nord de Peter Brook.

---

## ✨ Fonctionnalités

- **39 théâtres & opéras** avec fiches détaillées
- **Carte interactive** (Leaflet + OpenStreetMap) avec marqueurs cliquables
- **Recherche** insensible aux accents (opéra → Opéra, chatelet → Châtelet)
- **Filtres par genre** : Opéra · Ballet · Classique · Contemporain · Comédie · Boulevard · Musical · Danse · Concert
- **Fiches détail** : description historique, adresse GPS, horaires, tarifs, capacité, année de fondation, spectacles emblématiques
- **Favoris** persistants (localStorage)
- **Bilingue FR / EN** complet
- **Design** : esthétique velours bordeaux & or, typographie Playfair Display

---

## 🏗️ Architecture

```
theatres-paris/
├── www/
│   └── index.html        # App complète en fichier unique
├── capacitor.config.json
├── package.json
└── ios/                  # Généré par Capacitor
```

L'app est un **single-file Capacitor app** : tout le HTML, CSS et JavaScript est contenu dans `www/index.html`.  
Pas de framework, pas de build step — copier `index.html` et synchroniser avec Xcode suffit.

---

## 🚀 Installation

### Prérequis
- Node.js ≥ 18
- Xcode ≥ 15
- CocoaPods

### Étapes

```bash
# 1. Cloner le repo
git clone https://github.com/migapple/theatres-paris.git
cd theatres-paris

# 2. Installer les dépendances
npm install

# 3. Ajouter la plateforme iOS
npx cap add ios

# 4. Synchroniser
npx cap sync ios

# 5. Ouvrir dans Xcode
npx cap open ios
```

Dans Xcode : sélectionner l'équipe de signature, brancher l'iPhone, ▶ Run.

> **Tip** : Pour les mises à jour ultérieures, il suffit de copier le nouveau `index.html` dans `www/` et de relancer depuis Xcode — pas besoin de `npx cap sync`.

---

## 📦 Dépendances

| Package | Version | Usage |
|---------|---------|-------|
| `@capacitor/core` | ^6.0.0 | Wrapper iOS natif |
| `@capacitor/ios` | ^6.0.0 | Plateforme iOS |
| Leaflet | 1.9.4 | Carte interactive (CDN) |
| Google Fonts | — | Playfair Display + Source Sans 3 (CDN) |
| CartoDB Voyager | — | Tuiles de carte (CDN) |

---

## 🗺️ Données

Les données des théâtres proviennent de :
- [Wikipédia — Liste des théâtres et opéras de Paris](https://fr.wikipedia.org/wiki/Liste_des_th%C3%A9%C3%A2tres_et_op%C3%A9ras_de_Paris)
- Sites officiels de chaque théâtre
- Coordonnées GPS vérifiées

---

## 📸 Captures d'écran

| Liste | Carte | Fiche détail |
|-------|-------|--------------|
| *(à venir)* | *(à venir)* | *(à venir)* |

---

## 📋 App Store

- **Bundle ID** : `com.michel.garlandat.scenesparis`  
- **Plateforme** : iOS 16+  
- **Langue principale** : Français  
- **Catégorie** : Voyage / Divertissement

---

## 📝 Licence

© 2026 Michel Garlandat. Tous droits réservés.  
Fait avec [Anthropic Claude](https://www.anthropic.com).

---

## 🤝 Autres apps

| App | Bundle ID | Description |
|-----|-----------|-------------|
| Musées Paris | `com.michel.garlandat.museesparis` | Guide des musées parisiens |
| Cimetières Paris | `com.michel.garlandat.cimetieres` | Guide Père-Lachaise & Montparnasse |
| MaCave | `com.michel.garlandat.macave` | Cave à vin personnelle |
| Frigo Manager | `com.michel.garlandat.frigomanager` | Gestion du réfrigérateur |
| MesRestaurants | `com.michel.garlandat.mesrestaurants` | Carnet de restaurants |
