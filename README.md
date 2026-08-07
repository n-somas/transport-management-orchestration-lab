# Transportation Management Orchestration Lab

Praxisnahes Portfolio-Projekt zur strukturierten Bearbeitung eines vereinfachten Transportation-Management-Prozesses mit Jira und Confluence.

Im Mittelpunkt stehen Anforderungsmanagement, Kanban-basierte Vorgangssteuerung, Transportkostenprüfung, Fehleranalyse, Akzeptanzkriterien, Testmanagement und nachvollziehbare Dokumentation.

> **Hinweis:** Dieses Repository ist ein eigenständiges Portfolio-Lab auf Basis eines fiktiven Transportation-Management-Szenarios. Es werden keine internen oder proprietären Unternehmensdaten verwendet.

## Projektziel

Ziel des Labs ist es zu zeigen, wie fachliche Anforderungen im Transportmanagement strukturiert erfasst, priorisiert, bearbeitet, getestet und dokumentiert werden können.

Das zentrale Szenario behandelt die Prüfung von Transportkosten. Dabei werden Grundfrachtraten, Mautzuschläge und weitere Kostenbestandteile betrachtet. Abweichungen zwischen erwarteten und tatsächlich berechneten Kosten sollen erkannt, analysiert und nachvollziehbar dokumentiert werden.

## Eingesetzte Werkzeuge und Methoden

- Jira
- Confluence
- Kanban
- Anforderungsmanagement
- User Stories
- Akzeptanzkriterien
- Testmanagement
- Soll-Ist-Vergleich
- Fehleranalyse
- Retest
- technische Dokumentation

## Jira-Struktur

Für das Szenario wurden unterschiedliche Jira-Vorgangstypen verwendet.

| Key | Typ | Beschreibung |
|---|---|---|
| KAN-5 | Epic | Transportkosten und Frachtenabrechnung optimieren |
| KAN-4 | Feature | Frachtenabrechnung transparenter gestalten |
| KAN-6 | Story | Kostenabweichungen nachvollziehen können |
| KAN-7 | Task | Prüfkriterien für Frachtraten definieren |
| KAN-8 | Bug | Mautzuschlag wird bei Kostenprüfung falsch berechnet |

Der Epic bündelt den übergeordneten fachlichen Themenbereich. Feature, Story, Task und Bug bilden unterschiedliche Arten der konkreten Arbeit innerhalb des Szenarios ab.

## Kanban-Workflow

Die Jira-Vorgänge wurden über einen definierten Kanban-Workflow gesteuert:

**Idee → Zu erledigen → In Bearbeitung → Im Test → Erledigt**

Die Status haben folgende Bedeutung:

| Status | Bedeutung |
|---|---|
| Idee | Eine neue Anforderung, Aufgabe oder ein Fehler wurde erfasst. |
| Zu erledigen | Der Vorgang wurde geprüft und zur Bearbeitung eingeplant. |
| In Bearbeitung | Die fachliche oder technische Bearbeitung läuft. |
| Im Test | Die Umsetzung wird anhand definierter Kriterien geprüft. |
| Erledigt | Prüfung und Bearbeitung wurden erfolgreich abgeschlossen. |

## User Story und Akzeptanzkriterien

Die Story `KAN-6` beschreibt die fachliche Anforderung, Kostenabweichungen nachvollziehen zu können.

Dafür wurden folgende Akzeptanzkriterien definiert:

- Erwartete und tatsächliche Transportkosten können gegenübergestellt werden.
- Abweichungen sind eindeutig erkennbar.
- Frachtraten und Zuschläge können getrennt geprüft werden.
- Die Ursache einer Abweichung kann dokumentiert werden.
- Das Prüfergebnis bleibt für andere Beteiligte nachvollziehbar.

## Beispiel einer Transportkostenprüfung

Im Testszenario wurde eine fehlerhafte Berechnung des Mautzuschlags simuliert.

| Kostenbestandteil | Soll | Ist |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 60 EUR |
| Gesamtkosten | 545 EUR | 560 EUR |
| Abweichung | 0 EUR | +15 EUR |

Der Soll-Ist-Vergleich zeigt eine Abweichung von 15 EUR.

Die Grundfrachtrate ist korrekt. Die Abweichung kann eindeutig dem Mautzuschlag zugeordnet werden.

## Fehleranalyse

Der Fehler wurde in Jira als Bug `KAN-8` dokumentiert.

Die Bearbeitung umfasste:

1. Fehlerbeschreibung
2. Soll-Verhalten
3. Ist-Verhalten
4. Schritte zur Reproduktion
5. Fehleranalyse
6. Korrektur
7. Retest
8. Abschlussprüfung

Die Analyse ergab, dass statt des erwarteten Mautzuschlags von 45 EUR ein Wert von 60 EUR berücksichtigt wurde.

## Retest

Nach der simulierten Korrektur wurde die Transportkostenberechnung erneut geprüft.

| Kostenbestandteil | Erwartet | Nach Korrektur |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 45 EUR |
| Gesamtkosten | 545 EUR | 545 EUR |
| Abweichung | 0 EUR | 0 EUR |

**Retest-Ergebnis: Bestanden**

Die erwarteten und tatsächlich berechneten Transportkosten stimmen überein. Die zuvor festgestellte Abweichung tritt nicht mehr auf.

## Zusammenspiel von Jira und Confluence

Jira wird im Lab zur operativen Steuerung der Arbeit eingesetzt.

Anforderungen, Aufgaben und Fehler werden als Vorgänge erfasst, priorisiert und durch den definierten Kanban-Workflow geführt.

Confluence ergänzt Jira um die fachliche Dokumentation. Dort wurden unter anderem folgende Inhalte dokumentiert:

- Projektübersicht
- Prozessbeschreibung
- Prüfkriterien
- Testfall
- Soll-Ist-Vergleich
- Fehleranalyse
- Korrektur
- Retest
- Testergebnis

Die relevanten Jira-Vorgänge wurden direkt in die Confluence-Dokumentation eingebunden. Dadurch bleiben Bearbeitungsstatus und fachliche Dokumentation miteinander verknüpft.

## Confluence-Struktur

Die Dokumentation besteht aus einer zentralen Projektseite und zwei Unterseiten:

**Transportation Management Orchestration Lab**

- Transportkostenprüfung und Testkonzept
- Prozessbeschreibung

## Im Projekt angewendete Kenntnisse

Das Portfolio-Lab zeigt praktische Arbeit mit:

- Jira-Vorgangsmanagement
- Epic, Feature, Story, Task und Bug
- Kanban-Workflows
- Anforderungsmanagement
- User Stories
- Akzeptanzkriterien
- funktionalen Tests
- Soll-Ist-Vergleichen
- Fehleranalyse
- Retesting
- Jira-Confluence-Verknüpfungen
- strukturierter fachlicher Dokumentation

## Projektstatus

Das definierte Szenario wurde vollständig bearbeitet.

Alle Jira-Vorgänge wurden durch den vorgesehenen Workflow geführt, getestet und auf den Status **Erledigt** gesetzt. Der übergeordnete Epic wurde nach Abschluss aller zugehörigen Vorgänge ebenfalls abgeschlossen.

Die fachliche Dokumentation wurde parallel in Confluence erstellt und mit den relevanten Jira-Vorgängen verknüpft.
