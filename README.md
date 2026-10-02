# Barista – Kaffee lernen

Lern-App fürs Handy: Barista-Praxis und SCA-Wissen in kurzen Quizrunden, mit Lernkarten und Aromarad.

**Live:** https://mvonulmerbach-ship-it.github.io/kaffee/

## Reiter

| Reiter | Fragen | Themen |
|---|---|---|
| ☕ Barista | 116 | Espresso-Grundlagen · Milch & Latte Art · Mahlen & Dosieren · Maschine & Wartung · Brühmethoden · Troubleshooting |
| 📐 SCA-Wissen | 128 | Extraktion & Kennzahlen · Cupping & Sensorik · Röstung · Wasser · Anbau & Verarbeitung · Green Grading & Defekte · Standards & Geschichte |
| 🎡 Aromarad | 33 | Aromarad & Sensorik, dazu das Aromarad zum Nachschlagen |

Insgesamt 277 Fragen in acht Fragetypen: Auswahl, Mehrfachauswahl, Wahr/Falsch, Ausreißer finden, Sortieren, Zuordnen, Lernkarte und Selbsttest.

## Funktionen

- **Alles gemischt** oder ein Thema wählen. Eine Runde hat bis zu 12 Fragen.
- Vor jedem Thema eine kurze **Lektion** mit den wichtigsten Punkten („Direkt zu den Fragen“ überspringt sie).
- Nach jeder Antwort die Auflösung mit Erklärung; am Ende Ergebnis, Bestwert je Thema, Punkte (⭐) und Tagesserie (🔥).
- In der Fußleiste des Quiz: 🎡 Aromarad und 📖 [Kaffee-Nachschlagewerk](https://mvonulmerbach-ship-it.github.io/kaffee-nachschlagewerk/) als Overlay.
- Hell/Dunkel oben rechts: ◐ System (Standard) · ☀️ Hell · 🌙 Dunkel.
- Lernstand, Punkte und Hell/Dunkel-Wahl liegen nur im Browser (`localStorage`, Schlüssel `kaffee_lern_v1`).

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | die ganze App (HTML, CSS, JavaScript, Fragen) |
| `aromarad.html` | Aromarad, Kopie aus dem Repo `aroma-rad` – dort ändern, dann kopieren |
| `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `icon-maskable.png` | Installation als App |
| `sw.js` | Service Worker für den Offline-Betrieb |

## Auf dem Handy installieren

Seite in Chrome öffnen → Menü ⋮ → „Zum Startbildschirm hinzufügen“ (Safari: Teilen → „Zum Home-Bildschirm“).

## Offline

Nach dem ersten Öffnen läuft die App ohne Netz (Service Worker, network first mit Cache als Rückfall). Das Kaffee-Nachschlagewerk im Overlay ist eine eigene App und braucht dafür Netz, solange es nicht selbst einmal geöffnet wurde.
