# vvvv gamma — UX-Prototyp

Klickbarer Prototyp zu den UX-Vorschlägen für vvvv gamma (Browser, Help, Packs, References, Settings).

## Öffnen

Die Seite ist rein statisch. Es braucht keinen Server und keine Installation.

- **Lokal:** `index.html` im Browser öffnen.
- **Online:** über GitHub Pages (siehe unten).

## Dateien

- `index.html` — die gesamte Oberfläche (HTML, CSS, JavaScript).
- `data.js` — echte Pack-Daten aus nuget.org (Stand: 25.11.2026). Erzeugt mit `tools/scripts/fetch_packs.py` im Projekt-Hauptordner.

## Versionen

- **Version 1:** Browser mit Tabs (Welcome, Help, Packs, Extensions, Shortcuts), References als eigenes Fenster.
- **Version 2:** gleichrangige, andockbare Fenster (Welcome, Help, Packs, Extensions, Settings, References). Fenster an der Titelleiste ziehen, am Rand teilt, in der Mitte stapelt es als Tab.

## Veröffentlichen mit GitHub Pages

1. Auf GitHub ein neues Repository anlegen (z. B. `vvvv-ux-prototype`).
2. Im Ordner `prototype` lokal:
   ```
   git remote add origin https://github.com/<benutzer>/<repo>.git
   git push -u origin main
   ```
3. Auf GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, Branch `main`, Ordner `/ (root)`.
4. Nach ein bis zwei Minuten ist die Seite unter `https://<benutzer>.github.io/<repo>/` erreichbar.

Bei einem privaten Repository ist Pages nur mit einem bezahlten GitHub-Konto verfügbar.
