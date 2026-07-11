# WSD – Datenschutzerklärung (GitHub Pages)

Statische Seiten: `index.html` (Deutsch) + `en.html` (Englisch).
Die App verlinkt auf **https://raynargg.github.io/wsd-privacy/** (Profil → Datenschutzerklärung,
String `privacy_policy_url` in `wsd-app`).

## Vor der Veröffentlichung ausfüllen (Pflicht, DSGVO)
In **beiden** HTML-Dateien die Platzhalter ersetzen:
- `[VOLLSTÄNDIGER NAME]` / `[FULL NAME]`
- `[STRASSE HAUSNUMMER]` / `[STREET ADDRESS]`
- `[PLZ ORT]` / `[POSTAL CODE, CITY]`

## Veröffentlichen (einmalig, ~2 Minuten)
```bash
cd d:/App/wsd-privacy
git init && git add . && git commit -m "privacy policy"
gh repo create wsd-privacy --public --source . --push
gh api repos/RaynarGG/wsd-privacy/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```
Danach ist die Seite unter https://raynargg.github.io/wsd-privacy/ erreichbar
(erster Deploy dauert wenige Minuten). Diese URL gehört in der **Play Console** unter
*App-Inhalte → Datenschutzerklärung*.

> Repo muss **public** sein (GitHub Pages im Free-Plan). Es enthält nur die Policy — keine Secrets.
