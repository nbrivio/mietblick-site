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
- `assets/mietblick-logo-dark.png` — Wortmarke (Header)
- `assets/mietblick-appicon-hero.png` / `.webp` — 3D Haus-Icon (Hero-Section, optimiert)
- `assets/mietblick-icon-180.png` — Favicon

**Screenshots:**
- `assets/screen-*.webp` — App-Screenshots (iPhone-Mockups)

Alle Bilder sind **webp-optimiert** für schnelleres Laden.

---

## 🔧 Architektur

**Stack:**
- **HTML5** — semantisch, keine Framework-Dependencies
- **CSS3** — inlined für schnelles Laden, Dark Mode unterstützt
- **Keine Externe Dependencies** — kein Google Fonts, kein Analytics, keine Tracking-Pixel
- **Responsiv** — Mobile-first Design

**Hosting:**
- GitHub Pages (`github.com/nbrivio/mietblick-site`)
- Domain: `mietblick-app.ch` (Hostpoint)
- HTTPS: Let's Encrypt (via GitHub Pages)

---

## 🚀 Änderungen vornehmen

Die Website wird direkt im Repository bearbeitet — **kein Build-Prozess nötig**.

### HTML/CSS bearbeiten
```bash
# 1. Repository klonen
git clone https://github.com/nbrivio/mietblick-site.git
cd mietblick-site

# 2. Änderungen vornehmen (z.B. index.html, style-Abschnitt)
vim index.html

# 3. Pushen → GitHub Pages deployt automatisch
git add -A
git commit -m "Update: ..."
git push origin main
```

### Assets hinzufügen
- Bilder → `assets/`
- Formate: PNG (Fallback), WebP (primär)
- Komprimiert & optimiert für Web

### Rechtstext aktualisieren
Texte in `datenschutz.html`, `nutzungsbedingungen.html` bearbeiten — **direkt im HTML**, nicht über einen Markdown-Build.

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
- Farben: Petrol (#1B3639), Lime (#C6FF28)
- Typo: Inter (System Font-Stack)
- Design System: `mietblick.-App` Referenz

---

## 📱 App-Store Links

```html
<!-- iOS App Store -->
<a href="https://apps.apple.com/ch/app/id6824303520">Im App Store laden</a>
```

---

## 🔐 Rechtliches

**Anbieterin:** Ryse Solutions KLG  
**UID:** CHE-268.832.753  
**Adresse:** Talackerstrasse 15, 5037 Muhen, Schweiz  
**Kontakt:** support@mietblick-app.ch

---

**Status:** ✅ Production-ready (v1.0.2)  
**Zuletzt aktualisiert:** 19. Oktober 2026
