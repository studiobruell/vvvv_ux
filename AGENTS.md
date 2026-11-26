# AGENTS.md — Kontext für Mitwirkende und KI-Agenten

## Zweck
Klickbarer Prototyp mit UX-Vorschlägen für vvvv gamma (Browser, Help, Packs, References, Settings, Extensions). Es ist kein Produktcode. Ziel ist, Entwicklern und Designern eine konkrete Diskussionsgrundlage zu geben.

## Aufbau
- `index.html` — die gesamte Oberfläche: HTML, CSS und JavaScript in einer Datei. Kein Build, kein Framework, kein Server nötig.
- `data.js` — echte Pack-Daten aus nuget.org (`window.PACK_DATA`). Erzeugt mit `tools/scripts/fetch_packs.py` im Projekt-Hauptordner. Nicht von Hand ändern.
- `README.md` — Kurzbeschreibung und Anleitung zum Veröffentlichen.

## Versionen
- **Version 1:** Browser mit Tabs (Welcome, Help, Packs, Extensions, Shortcuts), References als eigenes Fenster.
- **Version 2:** gleichrangige, andockbare Fenster. Fenster an der Titelleiste ziehen. Am Rand des Ziels teilt es die Fläche, in der Mitte stapelt es als Tab.
- Welche Version gilt, ist noch offen. Beide Versionen müssen beim Ändern funktionieren.

## Wo die Begründungen stehen
- Die Notizen am Rand jedes Screens (`NOTES`) erklären, was geändert wurde und welches Problem es löst.
- Die Flows (`FLOWS`) führen durch die wichtigsten Stellen. Hotspots markieren den nächsten Klick.
- Die ausführliche Screencast-Analyse liegt nicht im Repository.

## Regeln für Änderungen
- Oberfläche und Notizen auf Deutsch. Produktnamen wie vvvv, Help, Packs, Reference bleiben unverändert.
- Keine Zugangsdaten, keine internen Informationen im Repository.
- `data.js` nur über das Skript neu erzeugen, nie von Hand bearbeiten.
- Nach jeder Änderung prüfen:
  - Syntax: den Script-Block mit `node --check` prüfen.
  - Alle Flows durchklicken, je ein Hotspot pro Schritt.
  - Keine Konsolenfehler.
  - Beide Versionen öffnen.
- Keine Screenshot-Pflicht, aber Layoutfragen mit DOM-Messung prüfen (z. B. Fensterhöhe, Abstände).

## Bekannte Lücken
- Toter Code: `neuHelpOld` und `helpDownload` werden nicht mehr benutzt und können entfernt werden.
- Das Andocken in Version 2 ist nur über die Baum-Logik geprüft, nicht mit echter Maus.
- Mehrere Notizen beschreiben den heutigen Stand als „Ist“. Das ist ein Hinweis auf vvvv gamma, keine Ist-Screens mehr im Prototyp.
