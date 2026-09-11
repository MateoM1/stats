# STATS website (GitHub Pages)

Static support + privacy pages for the App Store listing. No build step.

## Publish (one time)

```bash
cd site
git init -b main
git add index.html privacy/index.html icon.jpg
git commit -m "STATS support site"
gh repo create MateoM1/stats --public --source . --push
```

(No `gh`? Create an empty public repo named `stats` at github.com/new, then
`git remote add origin https://github.com/MateoM1/stats.git && git push -u origin main`.)

Then enable Pages: repo → Settings → Pages → Source: **Deploy from a branch** →
Branch: **main**, folder **/ (root)** → Save. Live in ~1 minute.

## URLs for App Store Connect

| Field | Value |
|---|---|
| Support URL | https://mateom1.github.io/stats/ |
| Privacy Policy URL | https://mateom1.github.io/stats/privacy/ |
| Marketing URL | (leave empty) |

## Updating

Edit the HTML, commit, push — Pages redeploys automatically. Both pages are
bilingual (EN/ES toggle, defaults to the browser language); edit both language
blocks when changing content. This folder is intentionally not part of the app
repo's history (it has its own `.git` after publishing).
