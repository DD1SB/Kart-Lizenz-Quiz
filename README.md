# Kart-Lizenz-Quiz

Kinderfreundlicher, statischer Lerntrainer für Fragen aus dem **„Fragenkatalog für DMSB-anerkannte Fahrer-Lizenzlehrgänge Kart“**.

## Stand dieser ersten Version

- Lernmodus mit zufälligen Fragen
- adaptive Gewichtung: neue bzw. häufig falsch beantwortete Fragen erscheinen öfter
- Kapitelwahl
- eigener Modus „Schwierige Fragen“
- Prüfungssimulation mit Fragenzahl und Zeitlimit
- zufällige Reihenfolge der Fragen und Antworten
- Lernstatistik in `localStorage`
- responsives Layout für Smartphone, Tablet und Desktop
- kein Backend und keine Anmeldung nötig
- derzeit 38 Fragen mit **vorläufig hinterlegten Lösungen**

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
