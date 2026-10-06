<!-- ELUCENIA technical documentation · vo2-e-mets · fr · no clinical/professional/rights approval -->

# VO₂ estimée, MET et capacité fonctionnelle

[conditions, sources et autorisations](https://elucenia.org/fr/outils/vo2-e-mets)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Durée d’exercice (Bruce)

`tempo`

min · intervalle: 1–27

### Âge

`idade`

ans · intervalle: 15–100

### Sexe

`sexo`

- `F` — Féminin
- `M` — Masculin

### Physiquement actif ?

`ativo`

- `0` — Non
- `1` — Oui

## Édition de la méthode

Foster 1984 polynôme Bruce; Bruce 1973 VO₂ âge/activité; MET=VO₂/3,5; FAI

## Formule documentée

VO₂ (Foster, Bruce): 14,8 − 1,379 × t + 0,451 × t² − 0,012 × t³ (mL/kg/min; t en minutes)

METs = VO₂ ÷ 3,5

VO₂ prédit (Bruce): hommes sédentaires 57,8 − 0,445 × âge; actifs 69,7 − 0,612 × âge; femmes sédentaires 42,3 − 0,356 × âge; actives 42,9 − 0,312 × âge

Déficit fonctionnel (FAI) = (VO₂ prédit − obtenu) ÷ VO₂ prédit × 100

## Limites et population

Le temps utilisé pour estimer le VO₂ doit être celui du protocole Bruce sur tapis roulant correspondant, pas la durée de n’importe quel exercice. L’équation donne une prédiction, pas une consommation d’oxygène mesurée par analyse des gaz. Le MET utilise la convention de 3,5 mL/kg/min ; il ne mesure pas le métabolisme de repos de la personne. Les références de capacité prévue et les associations pronostiques sont propres à la population : Myers 2002 a étudié des hommes adressés pour un test clinique. N’extrapolez pas automatiquement aux enfants, à d’autres protocoles ou au risque individuel de décès.

## Références

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Bonne capacité fonctionnelle

| Détails du résultat | |
| --- | --- |
| VO₂ estimée | 30,2 mL/kg/min |
| VO₂ prévue | 35,6 mL/kg/min |
| Déficit fonctionnel (FAI) | 15% |


### 2

Capacité fonctionnelle moyenne

| Détails du résultat | |
| --- | --- |
| VO₂ estimée | 20,2 mL/kg/min |
| VO₂ prévue | 35,6 mL/kg/min |
| Déficit fonctionnel (FAI) | 43% |

