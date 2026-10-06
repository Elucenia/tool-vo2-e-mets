<!-- ELUCENIA technical documentation · vo2-e-mets · de · no clinical/professional/rights approval -->

# Geschätztes VO₂, MET und funktionelle Leistungsfähigkeit

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/vo2-e-mets)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Belastungsdauer (Bruce)

`tempo`

min · Bereich: 1–27

### Alter

`idade`

Jahre · Bereich: 15–100

### Geschlecht

`sexo`

- `F` — Weiblich
- `M` — Männlich

### Körperlich aktiv?

`ativo`

- `0` — Nein
- `1` — Ja

## Fassung der Methode

Foster 1984 Bruce-Polynom; Bruce 1973 VO₂ Alter/Aktivität; MET=VO₂/3,5; FAI

## Dokumentierte Formel

VO₂ (Foster, Bruce): 14,8 − 1,379 × t + 0,451 × t² − 0,012 × t³ (mL/kg/min; t in Minuten)

METs = VO₂ ÷ 3,5

VO₂-Soll (Bruce): inaktive Männer 57,8 − 0,445 × Alter; aktive Männer 69,7 − 0,612 × Alter; inaktive Frauen 42,3 − 0,356 × Alter; aktive Frauen 42,9 − 0,312 × Alter

Funktionelle Beeinträchtigung (FAI) = (VO₂-Soll − gemessen) ÷ VO₂-Soll × 100

## Grenzen und Population

Die Zeit zur Schätzung von VO₂ muss aus dem entsprechenden Bruce-Laufbandprotokoll stammen, nicht aus beliebigem Training. Die Gleichung liefert eine Vorhersage, keinen per Gasanalyse gemessenen Sauerstoffverbrauch. MET verwendet die Konvention von 3,5 mL/kg/min; sie misst nicht den individuellen Ruhestoffwechsel. Referenzwerte der vorhergesagten Leistungsfähigkeit und prognostische Zusammenhänge sind populationsspezifisch: Myers 2002 untersuchte Männer, die zu klinischen Tests überwiesen wurden. Extrapolieren Sie nicht automatisch auf Kinder, andere Protokolle oder das individuelle Sterberisiko.

## Referenzen

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

Gute funktionelle Kapazität

| Ergebnisdetails | |
| --- | --- |
| Geschätztes VO₂ | 30,2 mL/kg/min |
| Vorhergesagtes VO₂ | 35,6 mL/kg/min |
| Funktionelles Defizit (FAI) | 15% |


### 2

Mäßige funktionelle Kapazität

| Ergebnisdetails | |
| --- | --- |
| Geschätztes VO₂ | 20,2 mL/kg/min |
| Vorhergesagtes VO₂ | 35,6 mL/kg/min |
| Funktionelles Defizit (FAI) | 43% |

