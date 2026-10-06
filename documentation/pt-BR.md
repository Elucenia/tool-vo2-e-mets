<!-- ELUCENIA technical documentation · vo2-e-mets · pt-BR · no clinical/professional/rights approval -->

# VO₂ estimado, METs e capacidade funcional

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/vo2-e-mets)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Tempo de exercício (Bruce)

`tempo`

min · intervalo: 1–27

### Idade

`idade`

anos · intervalo: 15–100

### Sexo

`sexo`

- `F` — Feminino
- `M` — Masculino

### Fisicamente ativo?

`ativo`

- `0` — Não
- `1` — Sim

## Edição do método

Foster 1984 polinomial Bruce; Bruce 1973 VO 2 poridade/atividade; METVO 2/3,5; FAI

## Fórmula documentada

VO₂ (Foster, Bruce): 14,8 − 1,379 × t + 0,451 × t² − 0,012 × t³ (mL/kg/min; t em minutos)

METs = VO₂ ÷ 3,5

VO₂ previsto (Bruce): homens sedentários 57,8 − 0,445 × idade; ativos 69,7 − 0,612 × idade; mulheres sedentárias 42,3 − 0,356 × idade; ativas 42,9 − 0,312 × idade

Déficit funcional (FAI) = (previsto − obtido) ÷ previsto × 100

## Limites e população

O tempo usado para estimar VO₂ deve ser o do protocolo de esteira Bruce correspondente, não a duração de qualquer exercício. A equação fornece uma previsão, não consumo de oxigênio medido por análise de gases. MET usa a convenção de 3,5 mL/kg/min; isso não mede o metabolismo de repouso da pessoa. Referências de capacidade prevista e associações prognósticas são específicas da população: Myers 2002 estudou homens encaminhados para teste clínico. Não extrapole automaticamente para crianças, outros protocolos ou risco individual de morte.

## Referências

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Capacidade funcional boa

| Detalhes do resultado | |
| --- | --- |
| VO₂ estimado | 30,2 mL/kg/min |
| VO₂ previsto | 35,6 mL/kg/min |
| Déficit funcional (FAI) | 15% |


### 2

Capacidade funcional regular

| Detalhes do resultado | |
| --- | --- |
| VO₂ estimado | 20,2 mL/kg/min |
| VO₂ previsto | 35,6 mL/kg/min |
| Déficit funcional (FAI) | 43% |

