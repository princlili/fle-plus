# FLE+ Initiative - Site web

Site web trilingue (français, anglais, allemand) pour l'initiative FLE+.

## Structure du projet

```
site/
├── index.html           # Page d'accueil (redirige vers /fr/)
├── css/
│   └── styles.css      # Styles CSS centralisés
├── fr/
│   └── index.html      # Version française
├── en/
│   └── index.html      # Version anglaise
└── de/
    └── index.html      # Version allemande
```

## Déploiement sur GitHub Pages

### 1. Créer le repository

```bash
cd site/
git init
git add .
git commit -m "Initial commit - FLE+ trilingual site"
```

### 2. Pousser sur GitHub

```bash
git remote add origin https://github.com/princlili/fle-plus.git
git branch -M main
git push -u origin main
```

### 3. Activer GitHub Pages

1. Aller dans **Settings** → **Pages**
2. Source: sélectionner **main** branch
3. Dossier: laisser **/ (root)**
4. Cliquer sur **Save**

Le site sera accessible à : `https://princlili.github.io/fle-plus/`

## Personnalisation

### Modifier les liens GitHub

Dans chaque fichier HTML (fr/index.html, en/index.html, de/index.html), remplacer :
- `princlili` par votre nom d'utilisateur GitHub
- `pr.vaucher@gmail.com` par votre adresse email

### Modifier les couleurs

Dans `css/styles.css`, ajuster les variables CSS :

```css
:root {
    --color-primary: #1e5a8e;        /* Bleu principal */
    --color-primary-dark: #164571;   /* Bleu foncé */
    --color-primary-light: #2563eb;  /* Bleu clair */
    --color-text: #2d3748;           /* Texte principal */
}
```

## Ajouter du contenu

Pour ajouter une nouvelle section, utilisez la structure suivante dans chaque fichier HTML :

```html
<section id="nouvelle-section">
    <h2>Titre de la section</h2>
    <p>Contenu de la section...</p>
    
    <h3>Sous-titre</h3>
    <p>Plus de contenu...</p>
</section>
```

N'oubliez pas d'ajouter le lien dans la navigation :

```html
<nav>
    <ul>
        <li><a href="#vision">Vision</a></li>
        <li><a href="#voies">Les 4 voies</a></li>
        <li><a href="#nouvelle-section">Nouvelle section</a></li>
        <li><a href="#contribuer">Contribuer</a></li>
    </ul>
</nav>
```

## Maintenance

- Tous les styles sont dans `css/styles.css` - un seul fichier à modifier pour tout le site
- Les trois versions linguistiques partagent le même CSS
- Pour ajouter une langue, créer un nouveau dossier (ex: `it/`) avec un `index.html`

## Accessibilité

Le site respecte les standards WCAG 2.1 AA :
- Navigation au clavier
- Contraste des couleurs conforme
- Structure sémantique HTML5
- Attributs ARIA appropriés
- Lien "skip to content" pour lecteurs d'écran

## Licence

### Contenu pédagogique

Le contenu pédagogique (textes, ressources, approches) est sous licence **Creative Commons BY-SA 4.0**.

[![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

Vous pouvez :
- ✅ Utiliser, modifier et partager le contenu
- ✅ Usage commercial autorisé
- ⚠️ Attribution obligatoire
- ⚠️ Modifications à partager sous la même licence

Voir [LICENSE.md](LICENSE.md) pour les détails.

### Code source

Le code source (HTML, CSS, JS) est sous licence **MIT**.

Voir [LICENSE-CODE.md](LICENSE-CODE.md) pour les détails.
