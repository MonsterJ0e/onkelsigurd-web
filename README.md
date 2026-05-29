# onkelsigurd-web

Kildefiler til hjemmesiden for **Scherffenberg Møllers Fond** (onkelsigurd.dk).

Statisk Bootstrap-side (4 sider). Oprindeligt hentet fra den gamle Simply.com-hosting
den 29. maj 2026 og gjort klar til **GitHub Pages**.

## Deployment (GitHub Pages)
- `main`-branchen serveres direkte af GitHub Pages — push = deploy.
- `CNAME` peger sitet på **onkelsigurd.dk**.
- `.nojekyll` slår Jekyll-processering fra, så filerne serveres som de er.
- HTTPS udstedes automatisk af GitHub (Let's Encrypt), når custom domain er aktivt.

### DNS (sættes hos domæne-/DNS-udbyderen — rør IKKE MX/mail)
- Apex `onkelsigurd.dk` → A-records til GitHub Pages (bekræft de aktuelle IP'er i GitHubs dokumentation).
- `www` → CNAME til `<bruger>.github.io`.

## Indhold (~650 KB)

| Sti | Beskrivelse |
|---|---|
| `index.html` | Forsiden |
| `ansoegning.html` | Ansøgning — viser **legat@onkelsigurd.dk** |
| `bestyrelse.html` | Bestyrelse — viser **bestyrelse@onkelsigurd.dk** |
| `stifteren.html` | Om stifteren Sigurd Scherffenberg Møller |
| `Content/` | bootstrap.css, extra_styles.css |
| `Scripts/` | bootstrap.js |
| `fonts/` | Bootstrap glyphicons (eot/svg/ttf/woff) |
| `img/` | foto.png, foto1.png, cream_pixels.png (CSS-baggrund) |

## Eksterne afhængigheder (CDN — ikke i repoet)
1. **jQuery** — `https://code.jquery.com/jquery.js` (kræves af bootstrap.js)
2. **Google Fonts (Dosis)** — `https://fonts.googleapis.com/css?family=Dosis:400,300,600`

> **Housekeeping udført 30. maj 2026:** Google Fonts-linket er ændret fra `http://`
> til `https://` i alle fire HTML-filer, så skrifttypen ikke blokeres som "mixed
> content", når sitet serveres over HTTPS. (jQuery var allerede `https://`.)
>
> Mulig fremtidig forbedring: pin jQuery til en konkret version
> (`https://code.jquery.com/jquery-1.11.x.min.js`) i stedet for den uversionerede URL.
