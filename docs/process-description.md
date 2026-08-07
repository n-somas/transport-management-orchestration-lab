# Prozessbeschreibung

## Prozessziel

Der Prozess beschreibt, wie fachliche Anforderungen, Aufgaben und Fehler im Transportation Management strukturiert erfasst, bearbeitet, geprüft und abgeschlossen werden.

Jira dient dabei zur Steuerung der Vorgänge, während Confluence die fachliche Dokumentation ergänzt.

## Kanban-Workflow

Die Vorgänge durchlaufen einen definierten Workflow vom ersten fachlichen Bedarf bis zum Abschluss.

| Status | Bedeutung |
|---|---|
| **Idee** | Eine neue Anforderung, Aufgabe oder ein Fehler wurde erfasst, aber noch nicht priorisiert. |
| **Zu erledigen** | Der Vorgang wurde geprüft und zur Bearbeitung eingeplant. |
| **In Bearbeitung** | Die fachliche oder technische Bearbeitung läuft. |
| **Im Test** | Die Umsetzung wird anhand definierter Kriterien geprüft. |
| **Erledigt** | Die Prüfung wurde erfolgreich abgeschlossen und der Vorgang ist beendet. |

**Workflow:** Idee → Zu erledigen → In Bearbeitung → Im Test → Erledigt

## Jira-Vorgangstypen

| Vorgangstyp | Funktion im Lab |
|---|---|
| **Epic** | Bündelt einen größeren fachlichen Themenbereich und fasst zusammengehörige Vorgänge zusammen. |
| **Feature** | Beschreibt eine größere fachliche Funktion innerhalb des Themenbereichs. |
| **Story** | Beschreibt eine fachliche Anforderung aus Sicht eines Anwenders und enthält prüfbare Akzeptanzkriterien. |
| **Task** | Beschreibt eine konkrete Arbeit, die durchgeführt und abgeschlossen werden muss. |
| **Bug** | Dokumentiert ein fehlerhaftes Verhalten inklusive Soll-Ist-Abweichung, Fehleranalyse, Korrektur und Retest. |

## Anwendung im Projekt

- **KAN-5 Epic** – Transportkosten und Frachtenabrechnung optimieren
- **KAN-4 Feature** – Frachtenabrechnung transparenter gestalten
- **KAN-6 Story** – Kostenabweichungen nachvollziehen können
- **KAN-7 Task** – Prüfkriterien für Frachtraten definieren
- **KAN-8 Bug** – Mautzuschlag wird bei Kostenprüfung falsch berechnet

## Bearbeitungsablauf

Die Arbeit beginnt mit der Erfassung eines fachlichen Bedarfs oder Problems in Jira.

Nach der Prüfung und Priorisierung wird der Vorgang in den Status **Zu erledigen** überführt. Sobald die Bearbeitung beginnt, wechselt er auf **In Bearbeitung**.

Nach Abschluss der fachlichen oder technischen Arbeit wird der Vorgang in **Im Test** verschoben. Dort erfolgt die Prüfung anhand definierter Akzeptanz- oder Prüfkriterien.

Nur wenn diese erfolgreich erfüllt sind, wird der Vorgang auf **Erledigt** gesetzt.

## Umgang mit Fehlern

Fehler werden als Bug dokumentiert.

Im verwendeten Testszenario wurden folgende Schritte durchgeführt:

1. Fehler erfassen
2. Soll-Verhalten dokumentieren
3. Ist-Verhalten dokumentieren
4. Fehler reproduzieren
5. Ursache analysieren
6. Korrektur dokumentieren
7. Retest durchführen
8. Ergebnis bestätigen

Dadurch bleibt der Weg von der Fehlererkennung bis zum Abschluss nachvollziehbar.

## Zusammenarbeit von Jira und Confluence

Jira wird in diesem Projekt zur operativen Steuerung der Arbeit verwendet. Anforderungen, Aufgaben und Fehler werden als Vorgänge erfasst, priorisiert und durch den definierten Kanban-Workflow geführt.

Confluence ergänzt Jira um die fachliche Dokumentation. Prüfkriterien, Testfälle, Soll-Ist-Vergleiche, Fehleranalysen und Testergebnisse werden dort strukturiert festgehalten.

Die relevanten Jira-Vorgänge sind direkt mit den Confluence-Seiten verknüpft, sodass Bearbeitungsstatus und Dokumentation gemeinsam nachvollziehbar bleiben.

## Ergebnis

Durch die Kombination aus Jira und Confluence entsteht ein durchgängiger Ablauf von der fachlichen Anforderung über Bearbeitung und Test bis zur abschließenden Dokumentation.
