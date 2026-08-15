# Kart-Lizenz-Quiz

Kinderfreundlicher, statischer Lerntrainer für Fragen aus dem **„Fragenkatalog für DMSB-anerkannte Fahrer-Lizenzlehrgänge Kart“**.

## Versionsstand

- **App:** v0.6
- **Quiz-Datenbestand:** v0.2, Stand 11.08.2026
- **DMSB-Quellkatalog:** Stand 01/2025
- **Lösungen/Erklärungen:** in fachlicher Prüfung

App-Version und Quiz-Datenbestand werden getrennt versioniert. Eine reine Korrektur an Lösung, QuickTipp oder Quellenangabe kann deshalb den Datenbestand erhöhen, ohne dass sich die Anwendung selbst ändert.

## Stand dieser Version

- Lernmodus mit zufälligen Fragen
- adaptive Gewichtung: neue bzw. häufig falsch beantwortete Fragen erscheinen öfter
- Kapitelwahl
- eigener Modus „Schwierige Fragen“
- Prüfungssimulation mit Fragenzahl und Zeitlimit
- zufällige Reihenfolge der Fragen und Antworten
- Lernstatistik in `localStorage`
- responsives Layout für Smartphone, Tablet und Desktop
- kein Backend und keine Anmeldung nötig
- vollständiger Katalog mit **111 Fragen** und vorläufig hinterlegter Lösungsschablone

> Der DMSB veröffentlicht zusammen mit dem Fragenkatalog keine Lösungsschablone. Die hinterlegten Lösungen sind deshalb nicht offiziell und müssen vor produktivem Einsatz fachlich geprüft werden.

## Lokal starten

Da die Fragen per `fetch()` aus JSON geladen werden, sollte die App über einen kleinen Webserver gestartet werden.

```bash
python -m http.server 8000
```

Danach im Browser `http://localhost:8000` öffnen.

## GitHub Pages

Das Repository kann ohne Build-Schritt veröffentlicht werden:

1. Dateien in ein GitHub-Repository pushen.
2. Repository **Settings → Pages** öffnen.
3. Als Quelle **Deploy from a branch** wählen.
4. Branch `main` und Ordner `/ (root)` auswählen.
5. Speichern.

Danach wird die Seite direkt von GitHub Pages ausgeliefert.

## Fragen ergänzen

Alle Inhalte liegen in `data/questions.json`. Eine Frage sieht so aus:

```json
{
  "id": "4.01",
  "chapter": 4,
  "question": "Welche Startarten sind im Kartsport möglich?",
  "answers": [
    { "text": "Rollender Start", "correct": true },
    { "text": "Le Mans-Start", "correct": false },
    { "text": "Stehender Start", "correct": true }
  ]
}
```

Damit kann der Fragenkatalog unabhängig von der Anwendung gepflegt oder ausgetauscht werden.

## Quelle

Fragentexte basieren auf dem öffentlich verfügbaren DMSB-Fragenkatalog Kart, Stand 01/2025. Dem Dokument liegen laut DMSB die Reglements 2024 zugrunde.

Dieses Projekt ist kein offizielles Angebot des DMSB.


## Kursmodus (v0.6)

Pilot für Kapitel 4 mit 7 kurzen Lerneinheiten, Verständnisfragen, lokal gespeichertem Kursfortschritt und direkter Verknüpfung zu passenden DMSB-Originalfragen. Die Kursinhalte liegen getrennt in `data/course.json`.


## Kursmodus – Redaktionsfassung v0.6

Alle 10 Kapitel sind als Kurs angelegt. Die DMSB-Fragen eines Kapitels werden erst freigeschaltet, wenn alle Lerneinheiten des Kapitels abgeschlossen sind. Dieser Stand ist ausdrücklich zur fachlichen Durchsicht gedacht (`courseVersion: 0.2`).


### GitHub Pages / Cache

Statische Assets tragen in v0.6 einen Versionsparameter; die JSON-Daten werden mit `cache: no-store` geladen. Dadurch sollten neue Deployments ohne alten Kursstand erscheinen.


## v0.7 – Lernfluss

- Weiterlernen direkt von der Startseite
- Kursfortschritt auf der Startseite
- Falsch beantwortete Verständnisfragen werden innerhalb der Lektion erneut gestellt
- Eine Lektion ist erst gemeistert, wenn jede Verständnisfrage mindestens einmal richtig beantwortet wurde
- Eigene Kapitel-Challenge nach Abschluss aller Lektionen; erst danach gezielte Wiederholung der Fehlerfragen
- Versions-/Startseiteninformationen bereinigt
