# mietblick-site

Die öffentliche Website von **mietblick** unter [mietblick-app.ch](https://mietblick-app.ch),
ausgeliefert über GitHub Pages.

## Was hier liegt

Nur das erzeugte Ergebnis. Die Quelle sind die Rechtstexte der App:
`05_App/mietblick/Resources/Legal/*.md` im Projektordner `KW42_Mietblick`.
Dort ändern, dann `06_Website/build.py` laufen lassen und den Inhalt von `dist/`
hierher kopieren und pushen.

```
cd 06_Website
python3 build.py
```

## Seiten

| Datei | Dient als |
|---|---|
| `index.html` | Startseite, Marketing URL |
| `datenschutz.html` | Privacy Policy URL (App-Store-Pflicht, Richtlinie 5.1.1) |
| `nutzungsbedingungen.html` | Terms of Use / EULA (Abo-Pflicht, Richtlinie 3.1.2) |
| `impressum.html` | Anbieterin, UID, Kontakt |
| `support.html` | Support URL (App-Store-Pflicht, Richtlinie 1.5) |

`CNAME` hält die eigene Domain, `.nojekyll` schaltet die Jekyll-Verarbeitung ab –
die Seiten sind fertiges HTML.

## Haltung

Keine externen Aufrufe: keine Webfonts, kein Analytics, keine Einbettungen.
Eine App, die verspricht, dass nichts das Gerät verlässt, lädt auf ihrer eigenen
Website nichts von Dritten nach. Darum auch kein Cookie-Banner – es gibt keine Cookies.

Anbieterin: Ryse Solutions KLG
