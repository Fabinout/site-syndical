# Guide de maintenance du site — Syndicat Local

Ce guide explique comment maintenir votre site sans aucune connaissance en code.

---

## Structure des fichiers

```
site-syndical/
├── index.html        → Page d'accueil
├── tracts.html       → Page des tracts
├── contact.html      → Page de contact
├── style.css         → Styles partagés (NOUVEAU)
├── tracts/           → DOSSIER où déposer vos PDF
│   └── exemple.pdf
└── README.md         → Ce guide
```

---

## Mise en ligne initiale (GitHub Pages) — à faire une seule fois

1. Créez un compte gratuit sur **github.com**
2. Cliquez sur **"New repository"** (nouveau dépôt)
3. Nommez-le : `votre-syndicat` (ou ce que vous voulez)
4. Cochez **"Public"**
5. Cliquez **"Create repository"**
6. Cliquez **"uploading an existing file"**
7. Glissez-déposez TOUS les fichiers du dossier `site-syndicat/`
8. Cliquez **"Commit changes"**
9. Allez dans **Settings → Pages → Branch : main → Save**
10. Votre site est en ligne à : `https://votre-compte.github.io/votre-syndicat/`

---

## Ajouter un tract chaque semaine (3 étapes)

### Étape 1 — Préparez votre PDF
Nommez votre fichier sans espaces ni accents, par exemple :
- `tract-2026-04-28.pdf`
- `tract-semaine-18.pdf`

### Étape 2 — Déposez le PDF sur GitHub
1. Allez sur votre dépôt GitHub
2. Cliquez sur le dossier `tracts/`
3. Cliquez **"Add file" → "Upload files"**
4. Glissez votre PDF
5. Cliquez **"Commit changes"**

### Étape 3 — Ajoutez la carte sur la page Tracts
1. Sur GitHub, cliquez sur le fichier `tracts.html`
2. Cliquez sur l'icône crayon ✏️ (en haut à droite)
3. Cherchez ce texte dans le fichier :
   ```
   <!-- Ajoutez vos prochains tracts ici en copiant le bloc ci-dessus -->
   ```
4. Juste **avant** cette ligne, copiez-collez ce bloc :

```html

<article class="tract-card">
    <div class="tract-thumb">📄</div>
    <div class="tract-body">
        <p class="tract-date">Semaine du XX mois AAAA</p>
        <h2 class="tract-title">Titre de votre tract</h2>
        <p class="tract-desc">Résumé en quelques mots de ce tract.</p>
        <a class="tract-link" href="tracts/votre-fichier.pdf" target="_blank">
            Télécharger le PDF ↓
        </a>
    </div>
</article>
```

5. Modifiez la date, le titre, le résumé, et le nom du fichier PDF
6. Cliquez **"Commit changes"**

Le site se met à jour automatiquement en 1-2 minutes.

---

## Modifier les infos de contact

1. Sur GitHub, cliquez sur `contact.html`
2. Cliquez sur le crayon ✏️
3. Cherchez les lignes marquées `<!-- MODIFIER : ... -->`
4. Changez l'email, le téléphone, l'adresse ou les horaires
5. Cliquez **"Commit changes"**

---

## Domaine personnalisé (optionnel, ~12€/an)

Si vous souhaitez une adresse comme `syndicat-xyz.fr` au lieu de `github.io` :
1. Achetez un domaine sur **gandi.net**, OVH, ou **o2switch.fr**
2. Dans GitHub → Settings → Pages → "Custom domain" → entrez votre domaine
3. Suivez les instructions de votre registrar pour configurer le DNS

---

## Besoin d'aide ?

En cas de problème, la documentation GitHub Pages est disponible sur :
**docs.github.com/fr/pages**
