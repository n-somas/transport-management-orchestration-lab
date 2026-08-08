# Fachliche Anforderungen an die Transportkostenprüfung

## Zweck

Dieses Dokument beschreibt die fachlichen Anforderungen für die Prüfung von Transportkosten im Transportation Management Orchestration Lab.

Ziel ist es, Transportkosten strukturiert zu vergleichen, Abweichungen nachvollziehbar zu erkennen und Prüfergebnisse eindeutig zu dokumentieren.

## Fachlicher Kontext

Transportkosten setzen sich aus mehreren Bestandteilen zusammen. Im Lab werden insbesondere Grundfrachtrate, Mautzuschlag und weitere Zuschläge betrachtet.

Die Prüfung muss ermöglichen, erwartete Kosten mit tatsächlich berechneten Kosten zu vergleichen und Abweichungen einzelnen Kostenbestandteilen zuzuordnen.

## Anforderungen

### REQ-001 Soll-Ist-Vergleich

Das System bzw. der Prüfprozess muss erwartete und tatsächlich berechnete Transportkosten gegenüberstellen können.

**Akzeptanzkriterien**

- Soll- und Ist-Werte sind getrennt erkennbar.
- Die Gesamtkosten können miteinander verglichen werden.
- Abweichungen werden nachvollziehbar ausgewiesen.

**Jira-Bezug:** `KAN-6`

### REQ-002 Prüfung einzelner Kostenbestandteile

Grundfrachtrate, Mautzuschläge und weitere Zuschläge müssen einzeln geprüft werden können.

**Akzeptanzkriterien**

- Die Grundfrachtrate ist separat nachvollziehbar.
- Der Mautzuschlag ist separat nachvollziehbar.
- Weitere Zuschläge können getrennt betrachtet werden.

**Jira-Bezug:** `KAN-7`

### REQ-003 Erkennung von Kostenabweichungen

Abweichungen zwischen erwarteten und tatsächlichen Transportkosten müssen eindeutig erkennbar sein.

**Akzeptanzkriterien**

- Die Höhe der Abweichung ist bestimmbar.
- Die Abweichung kann einem Kostenbestandteil zugeordnet werden.
- Die Ursache kann dokumentiert werden.

**Jira-Bezug:** `KAN-6`, `KAN-8`

### REQ-004 Nachvollziehbare Fehlerdokumentation

Fehlerhafte Kostenberechnungen müssen strukturiert dokumentiert und reproduzierbar beschrieben werden können.

**Akzeptanzkriterien**

- Soll-Verhalten ist dokumentiert.
- Ist-Verhalten ist dokumentiert.
- Schritte zur Reproduktion sind vorhanden.
- Die Fehlerursache kann beschrieben werden.

**Jira-Bezug:** `KAN-8`

### REQ-005 Retest nach Korrektur

Nach einer Korrektur muss die Transportkostenprüfung erneut durchgeführt werden.

**Akzeptanzkriterien**

- Die korrigierte Berechnung wird mit denselben Prüfkriterien getestet.
- Soll- und Ist-Werte stimmen nach erfolgreicher Korrektur überein.
- Der zuvor festgestellte Fehler lässt sich nicht erneut reproduzieren.
- Das Retest-Ergebnis wird dokumentiert.

**Jira-Bezug:** `KAN-8`

### REQ-006 Nachvollziehbare Dokumentation

Prüfkriterien, Testergebnisse und Fehleranalysen müssen so dokumentiert werden, dass andere Beteiligte den Ablauf nachvollziehen können.

**Akzeptanzkriterien**

- Prüfkriterien sind dokumentiert.
- Testdaten und Ergebnisse sind dokumentiert.
- Fehleranalyse und Retest sind dokumentiert.
- Relevante Jira-Vorgänge sind mit der fachlichen Dokumentation verknüpft.

**Jira-Bezug:** `KAN-5`, `KAN-4`, `KAN-6`, `KAN-7`, `KAN-8`

## Traceability Matrix

| Requirement | Beschreibung | Jira-Vorgang | Nachweis |
|---|---|---|---|
| REQ-001 | Soll-Ist-Vergleich | KAN-6 | Testkonzept |
| REQ-002 | Einzelprüfung der Kostenbestandteile | KAN-7 | Prüfkriterien |
| REQ-003 | Erkennung von Kostenabweichungen | KAN-6, KAN-8 | Testfall und Fehleranalyse |
| REQ-004 | Fehlerdokumentation | KAN-8 | Bug-Dokumentation |
| REQ-005 | Retest nach Korrektur | KAN-8 | Retest-Ergebnis |
| REQ-006 | Nachvollziehbare Dokumentation | KAN-5, KAN-4, KAN-6, KAN-7, KAN-8 | Confluence-Dokumentation |

## Ergebnis

Die Anforderungen decken den vollständigen fachlichen Ablauf der Transportkostenprüfung ab: von der Erfassung und Prüfung einzelner Kostenbestandteile über die Identifikation von Abweichungen bis zur Fehleranalyse, Korrektur und erneuten Prüfung.
