# Prüfung der Lösungsschablone

Der öffentliche DMSB-Fragenkatalog Kart, Stand 01/2025, enthält 111 Fragen, aber keine offizielle Lösungsschablone. Die in `data/questions.json` hinterlegten Lösungen sind daher ein Arbeitsstand.

Jede Frage enthält zusätzlich `solutionStatus: "provisional"` sowie `solutionConfidence` (`high`, `medium` oder `low`). Diese Felder werden von der Web-App derzeit nicht ausgewertet und dienen nur der redaktionellen Prüfung.

Besonders gegenzuprüfen sind derzeit die mit `solutionConfidence: "low"` markierten Fragen. Vor einer öffentlichen Verwendung sollte die Lösungsschablone gegen die für den Fragenkatalog maßgeblichen DMSB-Reglements 2024 bzw. eine Auskunft des Lehrgangsanbieters/DMSB abgeglichen werden.

Hinweis: Frage 3.10 ist im Original als Matrix aufgebaut. Für die Web-App wurde sie in einzelne Zuordnungs-Antworten umgeformt, ohne die vier abgefragten Wettbewerbe zu verändern. Frage 8.9 wurde intern als `8.09` normalisiert.
