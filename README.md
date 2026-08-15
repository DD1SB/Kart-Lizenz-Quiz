# Kart-Lizenz-Trainer

Kinderfreundliche Webanwendung zur Vorbereitung auf DMSB-anerkannte Fahrer-Lizenzlehrgänge Kart.

> **v0.9 RC = Feature Freeze für v1.0.** Danach nur fachliche/textliche Korrekturen und Bugfixes.

## Versionsstand
- App: **v0.9 RC**
- Quiz-Daten: **v0.2**
- Kurs: **v0.2**
- DMSB-Fragenkatalog: **01/2025 · 111 Fragen**
- Status: **fachliche Prüfung vor v1.0**

## Funktionsumfang
111 DMSB-Fragen; adaptiver Lernmodus; 10 Kurskapitel mit 34 Lerneinheiten und 71 Verständnisfragen; Kapitel-Challenges; Prüfungssimulation; Statistik; Vorlesefunktion; Review-IDs; responsive Oberfläche; lokale Speicherung ohne Backend.

Details: [`docs/FEATURES.md`](docs/FEATURES.md).

## Fachlicher Review
Der Fragenkatalog enthält im Projekt keine offizielle Lösungsschablone. Lösungen, QuickTipps, Quellen und Kursinhalte sind Arbeitsstände.

**Zum Korrekturlesen bitte mit [`docs/REVIEW.md`](docs/REVIEW.md) beginnen.**

Weitere Dokumente: [`solutions-review.md`](docs/solutions-review.md), [`COURSE.md`](docs/COURSE.md), [`EXAM.md`](docs/EXAM.md), [`DATA.md`](docs/DATA.md), [`KNOWN-ISSUES.md`](docs/KNOWN-ISSUES.md), [`CHANGELOG.md`](docs/CHANGELOG.md).

## Prüfung
30 zufällige Fragen; 60 Minuten regulär, 90/120 Minuten Übungsmodus. Maximalpunkte je Frage = Anzahl richtiger Antworten. Nur richtige unvollständige Auswahl gibt Teilpunkte; jede falsche Auswahl = 0 Punkte für die Frage. Bestanden ab 65 %.

## Lokal starten
```bash
python -m http.server 8000
```

## GitHub Pages
Settings → Pages → Deploy from a branch → `main` → `/ (root)`. Ordnerstruktur `css/`, `js/`, `data/`, `docs/` erhalten.

## Einordnung
Kein offizielles Angebot des DMSB oder ADAC. Fragentexte basieren auf dem DMSB-Fragenkatalog Kart 01/2025. Laut Katalog liegen DMSB-Reglements 2024 zugrunde; Quellenhinweise mit neueren Regelständen sind Teil des Reviews.
