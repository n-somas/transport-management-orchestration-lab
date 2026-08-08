# TC-001 – Transportkostenabweichung erkennen

## Testfall-ID

`TC-001`

## Titel

Transportkostenabweichung beim Mautzuschlag erkennen und nachvollziehen

## Testziel

Prüfen, ob eine Abweichung zwischen erwarteten und tatsächlich berechneten Transportkosten erkannt und eindeutig einem Kostenbestandteil zugeordnet werden kann.

## Verknüpfte Anforderungen

- `REQ-001` – Soll-Ist-Vergleich
- `REQ-002` – Prüfung einzelner Kostenbestandteile
- `REQ-003` – Erkennung von Kostenabweichungen
- `REQ-004` – Nachvollziehbare Fehlerdokumentation
- `REQ-005` – Retest nach Korrektur

## Jira-Bezug

- `KAN-6` – Kostenabweichungen nachvollziehen können
- `KAN-7` – Prüfkriterien für Frachtraten definieren
- `KAN-8` – Mautzuschlag wird bei Kostenprüfung falsch berechnet

## Voraussetzungen

- Eine Grundfrachtrate ist hinterlegt.
- Ein Mautzuschlag kann separat geprüft werden.
- Erwartete und tatsächlich berechnete Transportkosten können gegenübergestellt werden.
- Die relevanten Prüfkriterien sind definiert.

## Testdaten

| Kostenbestandteil | Soll | Ist |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 60 EUR |
| Gesamtkosten | 545 EUR | 560 EUR |
| Abweichung | 0 EUR | +15 EUR |

## Testschritte

| Schritt | Aktion | Erwartetes Ergebnis |
|---|---|---|
| 1 | Transportkostenprüfung öffnen | Grundfrachtrate und Zuschläge sind prüfbar. |
| 2 | Grundfrachtrate von 500 EUR prüfen | Soll- und Ist-Wert stimmen überein. |
| 3 | Mautzuschlag prüfen | Erwarteter Wert beträgt 45 EUR. |
| 4 | Tatsächlich berechneten Mautzuschlag vergleichen | Ist-Wert von 60 EUR wird erkannt. |
| 5 | Gesamtkosten vergleichen | Eine Abweichung von 15 EUR wird festgestellt. |
| 6 | Ursache der Abweichung analysieren | Die Abweichung kann eindeutig dem Mautzuschlag zugeordnet werden. |
| 7 | Prüfergebnis dokumentieren | Ursache und Ergebnis sind nachvollziehbar festgehalten. |

## Erwartetes Ergebnis

Die Kostenabweichung wird erkannt und eindeutig dem Mautzuschlag zugeordnet.

Die Grundfrachtrate ist korrekt. Der Mautzuschlag weicht um 15 EUR vom erwarteten Wert ab.

## Tatsächliches Ergebnis

Die Grundfrachtrate beträgt wie erwartet 500 EUR.

Der Mautzuschlag beträgt jedoch 60 EUR statt 45 EUR. Dadurch ergeben sich Gesamtkosten von 560 EUR statt 545 EUR.

**Festgestellte Abweichung: +15 EUR**

## Testergebnis

**Status: Fehler festgestellt**

Der Testfall zeigt, dass die Abweichung erkannt und eindeutig dem Mautzuschlag zugeordnet werden kann.

Der festgestellte Fehler wird unter `KAN-8` dokumentiert.

## Fehleranalyse

Die Differenz entsteht ausschließlich durch den fehlerhaften Mautzuschlag.

- Grundfrachtrate: korrekt
- Erwarteter Mautzuschlag: 45 EUR
- Tatsächlicher Mautzuschlag: 60 EUR
- Abweichung: +15 EUR

## Korrektur im Testszenario

Die Berechnungsregel für den Mautzuschlag wird so angepasst, dass statt 60 EUR der erwartete Wert von 45 EUR berücksichtigt wird.

## Retest

Nach der Korrektur wird derselbe Testfall erneut ausgeführt.

| Kostenbestandteil | Erwartet | Nach Korrektur |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 45 EUR |
| Gesamtkosten | 545 EUR | 545 EUR |
| Abweichung | 0 EUR | 0 EUR |

## Retest-Ergebnis

**Status: Bestanden**

Die Soll- und Ist-Werte stimmen nach der Korrektur überein.

Der zuvor festgestellte Fehler beim Mautzuschlag tritt nicht mehr auf und kann im Retest nicht erneut reproduziert werden.

## Abschluss

Der Testfall bestätigt, dass Transportkostenabweichungen erkannt, einzelnen Kostenbestandteilen zugeordnet und nach einer Korrektur durch einen Retest überprüft werden können.
