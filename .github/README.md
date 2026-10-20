# mietblick-site

Die öffentliche Website von **mietblick** unter [mietblick-app.ch](https://mietblick-app.ch), ausgeliefert über **GitHub Pages**.

---

## 📋 Inhalt

| Datei | Zweck | Link |
|-------|-------|------|
| `index.html` | Startseite, Marketing & Conversion | / |
| `datenschutz.html` | Datenschutzerklärung (nDSG) | /datenschutz |
| `nutzungsbedingungen.html` | Nutzungsbedingungen & Abo | /nutzungsbedingungen |
| `impressum.html` | Anbieterin, UID, Kontakt | /impressum |
| `support.html` | Support-Kontakt | /support |

---

## 🎨 Assets

**Logos & Icons:**
- `assets/wortmarke-petrol.png`: Wortmarke für hellen Grund (Header, Fuss)
- `assets/wortmarke-weiss.png`: Wortmarke für Dunkelmodus
- `assets/hero-haus.webp`: Bildmarke im Hero
- `assets/mark.webp`: freigestellte Bildmarke im Abschlussband
- `assets/icon.png` / `assets/appicon.png`: Favicon und Vorschaubild

**Screenshots:** echte Bildschirme aus der App
- `assets/app-zuhause.webp`, `app-vertrag.webp`, `app-kuendigen.webp`,
  `app-einordnung.webp`, `app-wohnung.webp`

**Illustrationen** (Style A, Soft Spatial 3D):
- `assets/einzug-zuhause.webp`, `geraet-defekt-kueche.webp`,
  `abnutzung-streichen.webp`, `kleine-veraenderung-lampe.webp`

Alle Bilder sind **webp-optimiert** für schnelleres Laden.

---

## 🔧 Architektur

**Stack:**
- **HTML5**: semantisch, keine Framework-Dependencies
- **CSS3**: inlined für schnelles Laden, Dark Mode unterstützt
- **Keine Externe Dependencies**: kein Google Fonts, kein Analytics, keine Tracking-Pixel
- **Responsiv**: Mobile-first Design

**Hosting:**
- GitHub Pages (`github.com/nbrivio/mietblick-site`)
- Domain: `mietblick-app.ch` (Hostpoint)
- HTTPS: Let's Encrypt (via GitHub Pages)

---

## 🚀 Änderungen vornehmen

**Die HTML-Dateien hier sind erzeugt, nicht von Hand gepflegt.** Quelle ist
`06_Website/build.py` im Projektordner `KW42_Mietblick`. Wer hier direkt editiert,
verliert die Änderung beim nächsten Build.

```bash
# im Projektordner
cd 06_Website
python3 build.py          # schreibt dist/

# Inhalt von dist/ in dieses Repository kopieren, dann
git add -A
git commit -m "..."
git push origin main      # GitHub Pages deployt automatisch
```

`CNAME`, `.nojekyll` und `.github/` bleiben dabei unberührt.

### Startseite ändern
Texte, Sektionen und Designsystem stehen in `build.py` (Abschnitte `CSS`, `SHELL`, `HOME`).

### Assets
Werden beim Build aus `01_Brand/` und `06_Website/assets/` erzeugt und auf Webgrösse
gerechnet. Neue App-Screenshots als `06_Website/assets/app-<name>.png` ablegen.

### Rechtstext aktualisieren
**Nicht hier.** Das Original liegt in `05_App/mietblick/Resources/Legal/*.md` und ist
zugleich die Fassung in der App. Dort ändern, Versionszeile hochzählen, neu bauen.
So können App und Website nicht auseinanderlaufen.

---

## ✅ Design-Prinzipien

**Privacy & Trust:**
- ❌ Keine externen Scripts
- ❌ Keine Cookies
- ❌ Keine Webfonts (System Fonts)
- ✅ Alles lokal, schnell, sicher

**Performance:**
- Inline CSS (kein separates Stylesheet)
- WebP Images mit PNG-Fallback
- Minimal JavaScript (keine Abhängigkeiten)
- Core Web Vitals optimiert

**Brand:**
- Farben: Petrol (#1B3639), Lime (#C5FF28), Ice (#F7FBFF)
- Typo: Inter (System Font-Stack)
- Design System: `mietblick.-App` Referenz

---

## 📱 App-Store Link

Die App ist eingereicht, aber noch nicht freigegeben. Die Seite zeigt darum
«Bald im App Store» und verlinkt bewusst nirgends hin.

Nach der Freigabe in `build.py` oben die URL eintragen:

```python
APPSTORE = "https://apps.apple.com/ch/app/id6824303520"
```

Hero und Abschlussband schalten dann automatisch auf einen echten Store-Button um.

---

## 🔐 Rechtliches

**Anbieterin:** Ryse Solutions KLG  
**UID:** CHE-268.832.753  
**Adresse:** Talackerstrasse 15, 5037 Muhen, Schweiz  
**Kontakt:** support@mietblick-app.ch

---

**Status:** ✅ Production-ready  
**Zuletzt aktualisiert:** 20. Oktober 2026
