# Beispiel: TRL definiert speziell für Apps für epidemiologische Studien 

Die nachfolgende Tabelle wurde auf Basis der NASA TRL-Tabelle und der oben genannten Software-TRLs speziell auf eine Domäne zugeschnitten: “App, um Symptome für epidemiologische Studien von Probanden zu sammeln, 
speichern und automatisiert auszuwerten”. Dabei wurde bewusst stark abstrahiert, um Kürze zu ermöglichen. Eine so verfeinerte Tabelle sollte es erlauben, besser zu entscheiden, welche SE-Methoden für welches 
Stadium sinnvoll sind.

| TRL | für Software | Beispiel | TRL für RS |
|-----|--------------|----------|------------|
| 1 | Hypothesenstadium | Es gibt evidente Anzeichen dafür, dass mit einer App für die automatisierte Auswertung epidemiologischen Studien besser unterstützt werden können. | demonstrierende Forschungssoftware |
| 2 | Machbarkeitsstadium | alle techn./rechtl. Fragen zur Machbarkeit geprüft; mögliche Frameworks und Designvorschläge wurden erarbeitet | |
| 3 | Einzelimplementierung | Einzelkomponenten zum Sammeln bzw. zum Auswerten wurden implementiert; funktionieren aber noch nicht im Verbund | |
| 4 | integrierte Implementierung | Alle Einzelkomponenten zum Sammeln, Speichern und Auswerten wurden implementiert und interagieren miteinander, was durch künstl. Testdaten geprüft wurde | prototypische Forschungssoftware |
| 5 | Interoperabilität mit anderen Systemen | App besitzt die notwendigen Schnittstellen, um Ergebnisse der Auswertung mit anderen Systemen auszutauschen | |
| 6 | Valide Funktionsweise  im realen Kontext | App wurde mit einer Dokumentation für die wesentlichen Anwendungsfälle ausgestattet und im Rahmen eines Feldversuchs mit Probanden getestet. | |
| 7 | Robuste Funktionsweise im realen Kontext für relevante Komponenten | Fehler in der Hauptfunktionalität (d. h., Sammeln, Speichern, Auswerten) wurden möglichst vollständig behoben und mehrmals in Feldstudien validiert. Dokumentation für die Entwicklung und Nutzung der Hauptfunktionalität ist ausreichend vorhanden. | robuste Forschungssoftware  |
| 8 | generell, robuste Funktionsweise im realen Kontext | Sämtliche Funktionalitätsprobleme bspw. auch die in der grafischen Nutzendenschnittstelle und eventuelle Performanzprobleme wurden möglichst behoben und im realen Feldversuch erfolgreich getestet | |
| 9 | mehrfach validierte, robuste Funktionsweise im realen Kontext | App wurde mehrmals erfolgreich für unterschiedliche epidemiologische Studien eingesetzt und die Qualitäts- und Weiterentwicklungsprozesse der App sowie der Dokumentation funktionieren | |

Kommentierende Anmerkungen für dieses Beispiel:
  * Die Einteilung suggeriert teilweise, dass eine Forschungssoftware zu einem bestimmten Zeitpunkt "fertig" ist. Das ist oft nicht der Fall, denn Software entwickelt sich mit der Forschungsfrage weiter analog zu den veränderten technischen Rahmenbedingungen. 
  * Die hier genutzte “Einzelimplementierung” (TRL3) ist nicht immer sinnvoll. Insbesondere agile Methoden forcieren die permanente Integration.
  * Begrifflichkeiten, wie zum Beispiel robust sind gegebenenfalls noch zu definieren. → Glossar
