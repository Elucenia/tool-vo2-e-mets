<!-- ELUCENIA technical documentation · vo2-e-mets · it · no clinical/professional/rights approval -->

# VO₂ stimato, MET e capacità funzionale

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/vo2-e-mets)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Durata dell’esercizio (Bruce)

`tempo`

min · intervallo: 1–27

### Età

`idade`

anni · intervallo: 15–100

### Sesso

`sexo`

- `F` — Femminile
- `M` — Maschile

### Fisicamente attivo?

`ativo`

- `0` — No
- `1` — Sì

## Edizione del metodo

Foster 1984 polinomio Bruce; Bruce 1973 VO₂ età/attività; MET=VO₂/3,5; FAI

## Formula documentata

VO₂ (Foster, Bruce): 14,8 − 1,379 × t + 0,451 × t² − 0,012 × t³ (mL/kg/min; t in minuti)

METs = VO₂ ÷ 3,5

VO₂ previsto (Bruce): uomini sedentari 57,8 − 0,445 × età; attivi 69,7 − 0,612 × età; donne sedentarie 42,3 − 0,356 × età; attive 42,9 − 0,312 × età

Deficit funzionale (FAI) = (VO₂ previsto − ottenuto) ÷ VO₂ previsto × 100

## Limiti e popolazione

Il tempo usato per stimare VO₂ deve provenire dal protocollo Bruce su tapis roulant corrispondente, non dalla durata di qualsiasi esercizio. L’equazione fornisce una previsione, non consumo di ossigeno misurato con analisi dei gas. MET usa la convenzione di 3,5 mL/kg/min; non misura il metabolismo a riposo della persona. I riferimenti di capacità prevista e le associazioni prognostiche sono specifici della popolazione: Myers 2002 ha studiato uomini inviati a test clinici. Non estrapolare automaticamente a bambini, altri protocolli o rischio individuale di morte.

## Riferimenti

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
