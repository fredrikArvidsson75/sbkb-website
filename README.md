# sbkb-website

Källkod för **sbkb.se** — Södra Bohusläns konsultbyrå (Fredrik Arvidsson, elkonsult).

## Stack

- Statisk HTML/CSS — ingen byggprocess
- Hostad på **GitHub Pages** + Cloudflare för CDN/DNS
- Designprofil i `../fredriks_trad/projekt/sbkb/BRAND.md` (Cormorant Garamond + Skog/Pergament/Koppar)

## Workflow

1. CC genererar HTML/CSS lokalt enligt BRAND.md
2. Granska och iterera lokalt (öppna `index.html` i browser)
3. `git add . && git commit -m "..." && git push`
4. GitHub Pages bygger automatiskt — live på sbkb.se inom ~30 sekunder

## Struktur

```
sbkb-website/
├── README.md          (denna fil)
├── .gitignore
├── CNAME              (sbkb.se — krävs för GitHub Pages custom domain)
├── index.html         (startsida)
├── css/
│   └── style.css      (med BRAND.md-tokens)
└── assets/            (logotyper, bilder)
    ├── sbkb-logo.svg
    └── sbkb-logo-vit.svg
```

## Sidor som planeras (enligt BRAND.md §6)

1. Start (index.html)
2. Tjänster — Projektering / Besiktning / Projektledning
3. Projekt — referenslista
4. Om oss
5. Kontakt

## Designprinciper (sammanfattning från BRAND.md)

- 60 % Skog (#1F3D2E), 30 % Pergament/Lin, 10 % Koppar (#A86F3C)
- Cormorant Garamond för rubriker, Inter för brödtext
- Raka linjer, `border-radius: 0` standard
- Inga gradienter, inga ikonfonts, inga emoji
- WCAG AAA på brödtext mot bakgrund

## Lokal preview

Öppna `index.html` direkt i webbläsaren, eller kör en lokal HTTP-server:

```bash
python -m http.server 8000
# Öppna http://localhost:8000
```

## Deploy

GitHub Pages är konfigurerad på `main`-branch:n. Pushar till `main` = live.
