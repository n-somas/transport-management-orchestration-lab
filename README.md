# Transportation Management Orchestration Lab

Praxisnahes Portfolio-Projekt zur strukturierten Bearbeitung eines vereinfachten Transportation-Management-Prozesses mit Jira und Confluence.

Im Mittelpunkt stehen Anforderungsmanagement, Kanban-basierte Vorgangssteuerung, Transportkostenprüfung, Fehleranalyse, Akzeptanzkriterien, Testmanagement und nachvollziehbare Dokumentation.

> Dieses Repository ist ein eigenständiges Portfolio-Lab auf Basis eines fiktiven Transportation-Management-Szenarios. Es werden keine internen oder proprietären Unternehmensdaten verwendet.

## Projektziel

Ziel des Labs ist es zu zeigen, wie fachliche Anforderungen im Transportmanagement strukturiert erfasst, priorisiert, bearbeitet, getestet und dokumentiert werden können.

Das zentrale Szenario behandelt die Prüfung von Transportkosten. Dabei werden Grundfrachtraten, Mautzuschläge und weitere Kostenbestandteile betrachtet. Abweichungen zwischen erwarteten und tatsächlich berechneten Kosten sollen eindeutig erkannt, analysiert und dokumentiert werden können.

## Eingesetzte Werkzeuge und Methoden

- Jira
- Confluence
- Kanban
- Requirements Management
- Akzeptanzkriterien
- Testmanagement
- Fehleranalyse
- Retest
- Soll-Ist-Vergleich
- strukturierte technische Dokumentation

## Jira-Struktur

| Key | Typ | Beschreibung |
|---|---|---|
| KAN-5 | Epic | Transportkosten und Frachtenabrechnung optimieren |
| KAN-4 | Feature | Frachtenabrechnung transparenter gestalten |
| KAN-6 | Story | Kostenabweichungen nachvollziehen können |
| KAN-7 | Task | Prüfkriterien für Frachtraten definieren |
| KAN-8 | Bug | Mautzuschlag wird bei Kostenprüfung falsch berechnet |

## Kanban-Workflow

```mermaid
flowchart LR
    A[Idee] --> B[Zu erledigen]
    B --> C[In Bearbeitung]
    C --> D[Im Test]
    D --> E[Erledigt]
