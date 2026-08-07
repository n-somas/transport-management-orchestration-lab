# Transportkostenprüfung und Testkonzept

## Ausgangssituation

Bei der Prüfung von Transportkosten müssen unterschiedliche Kostenbestandteile wie Grundfrachtrate, Mautzuschläge und weitere Zuschläge nachvollziehbar bewertet werden.

Abweichungen zwischen erwarteten und tatsächlich berechneten Kosten sollen eindeutig erkannt, einer Ursache zugeordnet und dokumentiert werden können.

## Ziel der Prüfung

Ziel ist ein strukturierter Soll-Ist-Vergleich der Transportkosten.

Die Prüfung soll sicherstellen, dass einzelne Kostenbestandteile nachvollziehbar sind, Abweichungen erkannt werden und Fehler nach einer Korrektur durch einen Retest überprüft werden können.

## Prüfkriterien

| Prüfpunkt | Erwartung | Prüfmethode |
|---|---|---|
| Grundfrachtrate | entspricht der vereinbarten Frachtrate | Soll-Ist-Vergleich |
| Mautzuschlag | wird nach definierter Regel berechnet | Einzelprüfung |
| Weitere Zuschläge | werden getrennt ausgewiesen | Einzelprüfung |
| Gesamtkosten | Summe der Kostenbestandteile ist korrekt | Berechnung prüfen |
| Abweichung | Ursache kann eindeutig zugeordnet werden | Abweichungsanalyse |

## Testfall 1 – Prüfung einer Transportkostenabweichung

Es wird geprüft, ob eine Abweichung zwischen erwarteten und tatsächlich berechneten Transportkosten erkannt und eindeutig einem Kostenbestandteil zugeordnet werden kann.

### Testdaten

| Kostenbestandteil | Soll | Ist |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 60 EUR |
| Gesamtkosten | 545 EUR | 560 EUR |
| Abweichung | 0 EUR | +15 EUR |

## Testergebnis

Der Soll-Ist-Vergleich zeigt eine Abweichung von 15 EUR.

Die Grundfrachtrate ist korrekt. Die Abweichung kann eindeutig dem Mautzuschlag zugeordnet werden.

Der Testfall deckt damit den in Jira unter `KAN-8` dokumentierten Fehler ab.

## Fehleranalyse

Die Abweichung von 15 EUR entsteht ausschließlich beim Mautzuschlag.

Die Grundfrachtrate von 500 EUR entspricht dem erwarteten Wert. Statt des erwarteten Mautzuschlags von 45 EUR werden jedoch 60 EUR berücksichtigt.

Damit ist die Ursache der Kostenabweichung eindeutig identifiziert.

## Korrektur

Die Berechnungsregel für den Mautzuschlag wurde im Testszenario korrigiert.

Der fehlerhafte Wert von 60 EUR wird durch den vorgesehenen Wert von 45 EUR ersetzt. Anschließend wird die Transportkostenberechnung erneut geprüft.

## Retest

| Kostenbestandteil | Erwartet | Nach Korrektur |
|---|---:|---:|
| Grundfrachtrate | 500 EUR | 500 EUR |
| Mautzuschlag | 45 EUR | 45 EUR |
| Gesamtkosten | 545 EUR | 545 EUR |
| Abweichung | 0 EUR | 0 EUR |

## Retest-Ergebnis

Der Retest wurde erfolgreich durchgeführt.

Die erwarteten und tatsächlich berechneten Transportkosten stimmen überein. Der zuvor festgestellte Fehler beim Mautzuschlag tritt nicht mehr auf und kann nicht erneut reproduziert werden.

## Gesamtergebnis

Die definierten Prüfkriterien wurden erfüllt.

Kostenbestandteile können einzeln geprüft, Soll- und Ist-Kosten gegenübergestellt und Abweichungen eindeutig einer Ursache zugeordnet werden.

Der festgestellte Fehler beim Mautzuschlag wurde korrigiert und durch einen erfolgreichen Retest bestätigt.

## Verknüpfte Jira-Vorgänge

- `KAN-6` – Kostenabweichungen nachvollziehen können
- `KAN-7` – Prüfkriterien für Frachtraten definieren
- `KAN-8` – Mautzuschlag wird bei Kostenprüfung falsch berechnet
