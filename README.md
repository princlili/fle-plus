# FLE+ Initiative - Site web

> Réinventer l'enseignement du français par les compétences transversales

🌐 **Site live** : https://princlili.github.io/fle-plus/

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](http://creativecommons.org/licenses/by-sa/4.0/)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE-CODE.md)

Site web trilingue (français, anglais, allemand) pour l'initiative FLE+.

---

## 📋 Table des matières

- [Structure du projet](#structure-du-projet)
- [Contribuer](#-contribuer)
- [Tester localement](#-tester-localement)
- [Déployer votre propre version](#déployer-votre-propre-version)
- [Personnalisation](#personnalisation)
- [Ajouter du contenu](#ajouter-du-contenu)
- [Maintenance](#maintenance)
- [Accessibilité](#accessibilité)
- [Licences](#licences)
- [Contact](#-contact)

---

## Structure du projet

```
site/
├── index.html              # Page d'accueil (redirige vers /fr/)
├── README.md               # Ce fichier
├── LICENSE.md              # Licence CC BY-SA 4.0 (contenu)
├── LICENSE-CODE.md         # Licence MIT (code)
├── CONTRIBUTING.md         # Guide détaillé de contribution
├── css/
│   └── styles.css         # Styles CSS centralisés
├── fr/
│   └── index.html         # Version française
├── en/
│   └── index.html         # Version anglaise
└── de/
    └── index.html         # Version allemande
```

---

## Contribuer

Nous accueillons chaleureusement les contributions ! Que vous soyez enseignant·e, développeur·euse, ou simplement intéressé·e par la pédagogie des langues, votre participation est précieuse.

### Avant de contribuer

1. **Lisez le guide complet** : [CONTRIBUTING.md](CONTRIBUTING.md)
2. **Consultez les issues existantes** : [Issues GitHub](https://github.com/princlili/fle-plus/issues)
3. **Ouvrez une discussion** pour les changements majeurs

### Workflow de contribution

```bash
# 1. Forker le repository sur GitHub
# Cliquez sur "Fork" en haut à droite de la page

# 2. Cloner votre fork
git clone https://github.com/VOTRE-USERNAME/fle-plus.git
cd fle-plus

# 3. Créer une branche pour votre contribution
git checkout -b amelioration-navigation
# Utilisez un nom descriptif : fix-typo-fr, add-italian, improve-css

# 4. Faire vos modifications
# Éditez les fichiers nécessaires...

# 5. Tester localement (voir section ci-dessous)
python3 -m http.server 8000
# Ouvrir http://localhost:8000 et vérifier vos changements

# 6. Commiter vos changements
git add .
git commit -m "Amélioration: navigation plus accessible"
# Utilisez des messages clairs et descriptifs

# 7. Pousser vers votre fork
git push origin amelioration-navigation

# 8. Ouvrir une Pull Request
# Sur GitHub, cliquez sur "Compare & pull request"
# Décrivez vos changements et leur motivation
```

### Types de contributions bienvenues

| Type | Exemples |
|------|----------|
| **Bugs** | Correction de liens cassés, erreurs de CSS, fautes de frappe |
| **Contenu** | Nouvelles ressources pédagogiques, amélioration des textes |
| **Traductions** | Ajout d'une nouvelle langue (italien, espagnol...) |
| **Accessibilité** | Amélioration du contraste, navigation clavier, ARIA |
| **Design** | Améliorations CSS, responsive, UX |
| **Documentation** | Clarification du README, guides, exemples |

### Standards de qualité

Toute contribution doit respecter :

- **Structure HTML/CSS existante** : Cohérence avec l'architecture actuelle
- **Accessibilité WCAG 2.1 AA** minimum : Contraste, navigation clavier, sémantique
- **Responsive design** : Tester sur mobile (320px), tablette (768px), desktop (1200px+)
- **Trois langues** : Si vous modifiez le contenu, adapter dans les 3 versions (ou signaler dans la PR)
- **Licences** : Tout contenu ajouté est sous CC BY-SA 4.0, code sous MIT

### Code de conduite

- Respectez les autres contributeurs
- Soyez constructif dans vos critiques
- Valorisez la diversité des approches pédagogiques
- Reconnaissez les limites de votre propre expérience

Pour plus de détails, consultez [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Tester localement

Avant de soumettre une pull request, **testez toujours vos modifications en local**.

### Option 1 : Python (recommandé - préinstallé sur Linux/Mac)

```bash
cd site/
python3 -m http.server 8000
```

### Option 2 : PHP

```bash
cd site/
php -S localhost:8000
```

### Option 3 : Node.js

```bash
cd site/
npx http-server -p 8000
```

### Option 4 : Extension VS Code

Si vous utilisez VS Code, installez l'extension **"Live Server"** et cliquez sur "Go Live".

---

Puis ouvrez votre navigateur à : **http://localhost:8000**

### Checklist de test

Avant de soumettre votre PR, vérifiez :

- [ ] Le site s'affiche correctement sur **desktop** (>900px)
- [ ] Le site s'affiche correctement sur **tablette** (600-900px)
- [ ] Le site s'affiche correctement sur **mobile** (<600px)
- [ ] Tous les **liens fonctionnent**
- [ ] Le **sélecteur de langue** fonctionne
- [ ] La **navigation au clavier** fonctionne (Tab, Enter)
- [ ] Les **trois versions linguistiques** sont cohérentes
- [ ] Pas d'erreurs dans la **console navigateur** (F12)

---

## Déployer votre propre version

Si vous souhaitez créer votre propre site basé sur FLE+, suivez ces étapes.

### 1. Forker et cloner

```bash
# Fork sur GitHub, puis :
git clone https://github.com/VOTRE-USERNAME/fle-plus.git
cd fle-plus
```

### 2. Personnaliser

Voir section [Personnalisation](#personnalisation) ci-dessous.

### 3. Créer votre repository

```bash
git init
git add .
git commit -m "Initial commit - Ma version FLE+"
git remote add origin https://github.com/VOTRE-USERNAME/mon-site-fle.git
git branch -M main
git push -u origin main
```

### 4. Activer GitHub Pages

1. Aller dans **Settings** → **Pages**
2. Source : sélectionner **main** branch
3. Folder : laisser **/ (root)**
4. Cliquer sur **Save**

Votre site sera accessible à : `https://VOTRE-USERNAME.github.io/mon-site-fle/`

---

## Personnalisation

### Informations de contact

Dans les fichiers suivants, remplacez :

| Fichier | Ligne | Remplacer |
|---------|-------|-----------|
| `fr/index.html` | 89, 93, 101 | `princlili` → votre username |
| `en/index.html` | 89, 93, 101 | `princlili` → votre username |
| `de/index.html` | 89, 93, 101 | `princlili` → votre username |
| `fr/index.html` | 89 | `pr.vaucher@gmail.com` → votre email |
| `en/index.html` | 89 | `pr.vaucher@gmail.com` → votre email |
| `de/index.html` | 89 | `pr.vaucher@gmail.com` → votre email |
| `LICENSE-CODE.md` | 7 | `[Votre Nom]` → votre nom |
| `CONTRIBUTING.md` | 49 | Email de contact |

### Modifier les couleurs

Dans `css/styles.css`, ajustez les variables CSS (lignes 16-21) :

```css
:root {
    --color-primary: #1e5a8e;        /* Bleu principal */
    --color-primary-dark: #164571;   /* Bleu foncé */
    --color-primary-light: #2563eb;  /* Bleu clair (liens) */
    --color-text: #2d3748;           /* Texte principal */
    --color-text-light: #4a5568;     /* Texte secondaire */
    --color-background: #ffffff;     /* Fond principal */
    --color-background-alt: #f7fafc; /* Fond alternatif */
    --color-border: #e2e8f0;         /* Bordures */
}
```

### Modifier les espacements

Ajustez les variables d'espacement (lignes 25-29) :

```css
:root {
    --spacing-xs: 0.5rem;   /* Extra petit */
    --spacing-sm: 1rem;     /* Petit */
    --spacing-md: 1.5rem;   /* Moyen */
    --spacing-lg: 2rem;     /* Grand */
    --spacing-xl: 3rem;     /* Extra grand */
}
```

---

## Ajouter du contenu

### Ajouter une nouvelle section

Dans chaque fichier HTML (`fr/index.html`, `en/index.html`, `de/index.html`) :

```html
<section id="ressources">
    <h2>Ressources pédagogiques</h2>
    <p>Introduction à la section...</p>
    
    <h3>Activités pour débutants</h3>
    <p>Description des activités...</p>
    
    <h3>Activités avancées</h3>
    <p>Description des activités...</p>
</section>
```

### Ajouter un lien de navigation

N'oubliez pas d'ajouter le lien dans la navigation :

```html
<nav role="navigation" aria-label="Navigation principale">
    <ul>
        <li><a href="#vision">Vision</a></li>
        <li><a href="#voies">Les 4 voies</a></li>
        <li><a href="#ressources">Ressources</a></li> <!-- ← Nouveau -->
        <li><a href="#contribuer">Contribuer</a></li>
    </ul>
</nav>
```

### Ajouter une nouvelle langue

1. Créer un nouveau dossier (ex: `it/` pour l'italien)
2. Copier `fr/index.html` dans `it/index.html`
3. Traduire le contenu
4. Ajouter l'option dans le sélecteur de langue :

```html
<div class="language-selector-content">
    <label>Langue:</label>
    <a href="../fr/index.html">Français</a>
    <a href="../en/index.html">English</a>
    <a href="../de/index.html">Deutsch</a>
    <a href="../it/index.html">Italiano</a> <!-- ← Nouveau -->
</div>
```

---

## Maintenance

### Structure du code

- **Un seul fichier CSS** (`css/styles.css`) contrôle tout le design
- Les **trois versions linguistiques** partagent le même CSS
- Modifier le CSS une fois = changement sur toutes les pages

### Bonnes pratiques

- Testez toujours en local avant de pousser
- Commitez régulièrement avec des messages clairs
- Vérifiez les trois versions linguistiques après toute modification de structure
- Validez votre HTML : [W3C Validator](https://validator.w3.org/)
- Testez l'accessibilité : [WAVE Tool](https://wave.webaim.org/)

### Commandes Git utiles

```bash
# Voir l'état des fichiers modifiés
git status

# Voir les différences avant de commiter
git diff

# Annuler des modifications locales
git restore fichier.html

# Voir l'historique
git log --oneline

# Revenir à un commit précédent
git revert <commit-hash>
```

---

## Accessibilité

Le site respecte les standards **WCAG 2.1 niveau AA** minimum.

### Fonctionnalités d'accessibilité

- **Navigation au clavier** : Tous les liens et interactions accessibles via Tab
- **Skip link** : Lien "Aller au contenu principal" pour éviter la navigation
- **Contraste** : Tous les textes respectent un ratio de contraste ≥ 4.5:1
- **Structure sémantique** : Utilisation correcte des balises HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- **Attributs ARIA** : Labels pour les zones de navigation
- **Responsive** : Adapté aux lecteurs d'écran et aux zooms jusqu'à 200%
- **Liens explicites** : Textes de liens descriptifs (pas de "cliquez ici")

### Tester l'accessibilité

**Outils recommandés :**
- [WAVE Browser Extension](https://wave.webaim.org/extension/)
- [axe DevTools](https://www.deque.com/axe/devtools/)
- [Lighthouse](https://developers.google.com/web/tools/lighthouse) (intégré à Chrome DevTools)

**Tests manuels :**
- Navigation complète au clavier (Tab, Shift+Tab, Enter)
- Test avec un lecteur d'écran (NVDA sur Windows, VoiceOver sur Mac)
- Zoom à 200% dans le navigateur

---

## Licences

Ce projet utilise une **double licence** pour distinguer le contenu pédagogique du code technique.

### Contenu pédagogique - CC BY-SA 4.0

Le contenu pédagogique (textes, ressources, approches, méthodologie) est sous licence **Creative Commons Attribution - Partage dans les Mêmes Conditions 4.0 International**.

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

**Vous êtes libre de :**
- **Partager** : Copier et redistribuer le contenu
- **Adapter** : Remixer, transformer et créer à partir du contenu
- **Usage commercial** : Utiliser le contenu à des fins commerciales

**Selon les conditions suivantes :**
- **Attribution** : Vous devez créditer l'œuvre, intégrer un lien vers la licence et indiquer si des modifications ont été effectuées
- **Partage dans les Mêmes Conditions** : Si vous modifiez le contenu, vous devez diffuser vos modifications sous la même licence

**Attribution suggérée :**
```
FLE+ Initiative par Pierre Vaucher
Licence CC BY-SA 4.0
https://github.com/princlili/fle-plus
```

Voir [LICENSE.md](LICENSE.md) pour le texte complet.

---

### Code source - MIT

Le code source (HTML, CSS, JavaScript) est distribué sous licence **MIT**.

**Vous êtes libre de :**
- Utiliser, copier, modifier, fusionner, publier, distribuer, sous-licencier et vendre le code
- Usage commercial sans restriction

**Condition :**
- Le copyright et la licence doivent être inclus dans toute copie substantielle

Voir [LICENSE-CODE.md](LICENSE-CODE.md) pour le texte complet.

---

### Pourquoi deux licences ?

- **Contenu pédagogique (CC BY-SA 4.0)** : Garantit que les ressources éducatives restent ouvertes et accessibles à tous, tout en protégeant contre l'appropriation fermée
- **Code source (MIT)** : Permet la réutilisation technique maximale sans contrainte, favorisant l'innovation et l'adaptation

---

## Contact

### Pour les contributions et questions techniques

- **Issues GitHub** : [github.com/princlili/fle-plus/issues](https://github.com/princlili/fle-plus/issues)
- **Pull Requests** : [github.com/princlili/fle-plus/pulls](https://github.com/princlili/fle-plus/pulls)
- **Discussions** : [github.com/princlili/fle-plus/discussions](https://github.com/princlili/fle-plus/discussions)

### Pour les questions générales sur le projet FLE+

- **Email** : pr.vaucher@gmail.com
- **Site web** : https://princlili.github.io/fle-plus/

---

## Remerciements

Merci à tous les contributeurs qui participent à faire évoluer l'enseignement du FLE !

---

**Fait avec ❤️ pour l'enseignement des langues**

*Dernière mise à jour : Novembre 2025*
