# Poof Landing

Landing minimaliste pour capturer les 500 premiers inscrits (Premium free for life).

## Local preview

Double-clique `index.html` — pas de build, pas de serveur.

## Étapes déploiement

### 1. Coller ton form Tally

1. Va sur https://tally.so → **Create new form**
2. Un seul champ : **Email** (required)
3. Bouton : `Claim my spot`
4. Onglet **Share** → **Embed** → copie l'iframe
5. Ouvre `index.html`, remplace le bloc entre `<!-- TALLY_EMBED_START -->` et `<!-- TALLY_EMBED_END -->` par l'iframe

### 2. Push sur GitHub

```bash
cd /Users/Uras/Desktop/poof-landing
git init
git add .
git commit -m "Poof landing v1"
git branch -M main
git remote add origin https://github.com/<ton-user>/poof-landing.git
git push -u origin main
```

### 3. Activer GitHub Pages

- GitHub repo → **Settings** → **Pages**
- Source : `Deploy from a branch`
- Branch : `main` / `/ (root)` → **Save**
- Ton URL : `https://<ton-user>.github.io/poof-landing/`

### 4. (Plus tard) Custom domain

- Réserve `poof.app` sur Namecheap/Porkbun
- Settings → Pages → Custom domain : `poof.app`
- Configure DNS (A records vers GitHub Pages IPs)

## Passer le compteur en live (à 100+ inscrits)

Aujourd'hui : le compteur affiche `First 500 spots — Premium free forever` (statique, aucun chiffre).

Quand tu dépasses 100 inscrits réels :
1. Ouvre `index.html`
2. Remplace la ligne `<p class="counter">...</p>` par un vrai compteur (Tally API ou Airtable)
3. Ping-moi et je te code le fetch en 5 min

## Structure

```
poof-landing/
├── index.html        → Landing 1-page
├── styles.css        → Design bleu ciel + halo
├── assets/
│   ├── icon-1024.png
│   ├── icon-192.png
│   └── apple-touch-icon.png
└── README.md
```
