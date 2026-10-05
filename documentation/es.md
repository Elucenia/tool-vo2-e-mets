<!-- ELUCENIA technical documentation · vo2-e-mets · es · no clinical/professional/rights approval -->

# VO₂ estimado, MET y capacidad funcional

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/vo2-e-mets)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Tiempo de ejercicio (Bruce)

`tempo`

min · intervalo: 1–27

### Edad

`idade`

años · intervalo: 15–100

### Sexo

`sexo`

- `F` — Femenino
- `M` — Masculino

### ¿Físicamente activo?

`ativo`

- `0` — No
- `1` — Sí

## Edición del método

Foster 1984 polinomio Bruce; Bruce 1973 VO₂ por edad/actividad; MET=VO₂/3,5; FAI

## Fórmula documentada

VO₂ (Foster, Bruce): 14,8 − 1,379 × t + 0,451 × t² − 0,012 × t³ (mL/kg/min; t en minutos)

METs = VO₂ ÷ 3,5

VO₂ previsto (Bruce): hombres sedentarios 57,8 − 0,445 × edad; activos 69,7 − 0,612 × edad; mujeres sedentarias 42,3 − 0,356 × edad; activas 42,9 − 0,312 × edad

Déficit funcional (FAI) = (VO₂ previsto − obtenido) ÷ VO₂ previsto × 100

## Límites y población

El tiempo usado para estimar VO₂ debe ser el del protocolo de cinta Bruce correspondiente, no la duración de cualquier ejercicio. La ecuación da una predicción, no consumo de oxígeno medido por análisis de gases. MET usa la convención de 3,5 mL/kg/min; no mide el metabolismo de reposo de la persona. Las referencias de capacidad prevista y las asociaciones pronósticas son específicas de la población: Myers 2002 estudió a hombres remitidos para pruebas clínicas. No extrapole automáticamente a niños, otros protocolos ni al riesgo individual de muerte.

## Referencias

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
