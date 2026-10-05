<!-- ELUCENIA technical documentation · vo2-e-mets · en · no clinical/professional/rights approval -->

# Estimated VO₂, METs and functional capacity

[conditions, sources and permissions](https://elucenia.org/en/tools/vo2-e-mets)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Exercise duration (Bruce)

`tempo`

min · range: 1–27

### Age

`idade`

years · range: 15–100

### Sex

`sexo`

- `F` — Female
- `M` — Male

### Physically active?

`ativo`

- `0` — No
- `1` — Yes

## Method edition

Foster 1984 Bruce polynomial; Bruce 1973 VO₂ by age/activity; MET=VO₂/3.5; FAI

## Documented formula

VO₂ (Foster, Bruce): 14.8 − 1.379 × t + 0.451 × t² − 0.012 × t³ (mL/kg/min; t in minutes)

METs = VO₂ ÷ 3.5

Predicted VO₂ (Bruce): sedentary men 57.8 − 0.445 × age; active men 69.7 − 0.612 × age; sedentary women 42.3 − 0.356 × age; active women 42.9 − 0.312 × age

Functional impairment (FAI) = (Predicted VO₂ − observed) ÷ Predicted VO₂ × 100

## Limits and population

The time used to estimate VO₂ must come from the corresponding Bruce treadmill protocol, not the duration of any exercise. The equation gives a prediction, not oxygen consumption measured by gas analysis. MET uses the convention of 3.5 mL/kg/min; it does not measure the person’s resting metabolism. Predicted-capacity references and prognostic associations are population-specific: Myers 2002 studied men referred for clinical testing. Do not automatically extrapolate to children, other protocols or an individual risk of death.

## References

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
