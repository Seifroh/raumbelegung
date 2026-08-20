# Interaktive Büroraumplanung

Browserbasiertes Zusatztool zur Unterstützung einer Büroraumplanung bei begrenzten Raumkapazitäten.

Das Tool entstand im Oktober 2025 im Rahmen einer konkreten internen Umzugsplanung. Ziel war es, unterschiedliche Raumbelegungen schnell ausprobieren zu können und dabei neben den verfügbaren Büroräumen auch Raummerkmale und Anwesenheitstage der Mitarbeitenden zu berücksichtigen.

## Funktionen

- Import strukturierter Planungsdaten
- Darstellung der verfügbaren Büroräume nach Gebäudeebenen
- Kennzeichnung relevanter Raummerkmale
- Zuordnung von Mitarbeitenden zu Räumen
- Drag-and-drop zwischen Räumen
- temporärer „Parkplatz“ für noch nicht zugeordnete Personen
- Erkennung möglicher Raumteilungen anhand überschneidungsfreier Arbeitstage
- visuelle Kennzeichnung freier Räume
- Speicherung eines Planungsstands
- erneutes Laden eines gespeicherten Planungsstands
- Zoomfunktion für größere Raumübersichten

## Hintergrund

Für eine größere Umzugsplanung mussten Büroräume neu verteilt werden. Da die Zahl flexibel nutzbarer Räume begrenzt war, sollten verschiedene Belegungsvarianten schnell miteinander verglichen werden können.

Nicht alle Räume eines Gebäudes sind Bestandteil der Planung. Funktionsgebundene Räume, die beispielsweise unmittelbar an bestimmte Arbeits- oder Therapiebereiche gekoppelt sind, werden bewusst nicht als frei verschiebbare Büroräume betrachtet.

Zusätzlich berücksichtigt das Tool die Anwesenheitstage der Mitarbeitenden. Personen ohne Überschneidung ihrer Arbeitstage können dadurch als mögliche Kandidaten für eine gemeinsame Raumnutzung erkannt werden.

## Verwendung

Die Anwendung läuft vollständig im Browser.

1. `index.html` im Browser öffnen.
2. Planungsdaten als CSV-Datei laden oder einen zuvor gespeicherten Planungsstand öffnen.
3. Mitarbeitende per Drag-and-drop zwischen den verfügbaren Räumen verschieben.
4. Hinweise auf mögliche Raumteilungen bei der Planung berücksichtigen.
5. Den aktuellen Planungsstand speichern, wenn die Bearbeitung später fortgesetzt werden soll.

Nicht gespeicherte Änderungen gehen beim Schließen der Seite verloren.

## Technischer Aufbau

**Frontend:** HTML, CSS, JavaScript  
**Datenverarbeitung:** Papa Parse, strukturierter Dateiimport  
**Zeichencodierung:** jschardet  
**Planungslogik:** regelbasierte Verarbeitung von Raum- und Personendaten sowie Vergleich von Anwesenheitstagen  
**Interaktion:** Drag-and-drop und dynamische DOM-Erzeugung  
**Persistenz:** dateibasierte Speicherung und Wiederherstellung von Planungsständen

Das Tool benötigt kein Backend und keine Datenbank.

## Projektstatus

Abgeschlossenes Praxisprojekt aus Oktober 2025.

Der aktuelle Stand wurde für eine konkrete Raumplanung entwickelt und eingesetzt. Es handelt sich bewusst um ein kleines, zweckgebundenes Werkzeug und nicht um ein vollständiges Raumverwaltungssystem.

Eine mögliche Weiterentwicklung wäre die automatisierte Übernahme von Anwesenheits- und Planungsdaten aus einem vorgelagerten Planungssystem.

## Datenschutz

Das Repository enthält keine produktiven Personen- oder Patientendaten.

Beispiel- und Testdaten sollten ausschließlich anonymisierte oder synthetische Daten enthalten.

## Hinweis

Das Projekt entstand als pragmatische Lösung für einen konkreten betrieblichen Planungsbedarf. Der Schwerpunkt lag auf schneller Nutzbarkeit und der Unterstützung der tatsächlichen Planung, nicht auf der Entwicklung eines universellen Softwareprodukts.