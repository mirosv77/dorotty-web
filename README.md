# Dorotty

Web spoločnosti Dorotty, s. r. o. – https://dorotty.cloud: údaje o firme, naše mobilné aplikácie, ich zásady ochrany osobných údajov, podmienky používania a stránky podpory.

Statický web: čisté HTML a jeden súbor CSS, bez JavaScriptu, knižníc a build kroku.

## Štruktúra
- `index.html` — úvodná stránka: firma, naše aplikácie, kontakt a identifikačné údaje
- `ochrana-osobnych-udajov.html` — zásady ochrany osobných údajov (slovenské, záväzné znenie)
- `privacy.html` — zásady po anglicky
- `datenschutz.html` — zásady po nemecky
- `gymdict/` — GymDict: o aplikácii a podpora (`index.html`), zásady ochrany súkromia (`sukromie.html`)
- `turista/` — Turista: o aplikácii a podpora (`index.html`), zásady ochrany súkromia (`sukromie.html`), podmienky používania (`podmienky.html`)
- `vyjazd/` — Výjazd: podpora, zásady ochrany súkromia, podmienky používania, zmluva o spracúvaní, zrušenie účtu a návod; stránky sa generujú z podkladov aplikácie, needituj ich ručne
- `404.html` — stránka „Stránka sa nenašla“
- `styl.css` — jediný štýl celého webu
- `sitemap.xml`, `robots.txt` — pre vyhľadávače
- `app-ads.txt` — súbor podľa štandardu app-ads.txt (overenie vydavateľa aplikácií)
- `_redirects` — presmerovania (`/modely/*` – sťahovanie modelov reči aplikácie GymDict)

Divočina a Včelín majú vlastné weby na https://divocina.dorotty.cloud a https://vcelin.dorotty.cloud – nie sú v tomto repozitári.

## Lokálny vývoj
Otvor `index.html` v prehliadači, alebo spusti:

```bash
python3 -m http.server 8000
```

a otvor http://localhost:8000. Tento jednoduchý server nepozná adresy bez `.html` (otvor napr. `/privacy.html` namiesto `/privacy`) a neuplatní `_redirects` ani `404.html`.

## Zverejnenie
- Vetva `main` sa automaticky zverejňuje na https://dorotty.cloud – celá, vrátane tohto súboru. Nedávaj sem nič, čo nemá byť verejné.
- Web nepoužíva analytiku, cookies, externé skripty ani písma a zásady ochrany osobných údajov to sľubujú – nepridávaj ich.
- Odkazy píš bez `.html` (`/privacy`, `/turista/`), v podpriečinkoch s absolútnou cestou (`/styl.css`).
