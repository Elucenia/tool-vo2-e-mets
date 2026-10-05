<!-- ELUCENIA technical documentation · vo2-e-mets · ar · no clinical/professional/rights approval -->

# VO₂ المقدر وMETs والقدرة الوظيفية

[الشروط والمصادر والأذونات](https://elucenia.org/ar/tools/vo2-e-mets)

## كيفية الاستخدام

استخدم الأداة في البوابة أو افتح index.html عبر خادم HTTP محلي. اختر اللغة، وأكمل الحقول، ثم أجرِ الحساب.

## المدخلات والوحدات

### زمن التمرين (Bruce)

`tempo`

min · النطاق: ١–٢٧

### العمر

`idade`

سنوات · النطاق: ١٥–١٠٠

### الجنس

`sexo`

- `F` — أنثى
- `M` — ذكر

### هل أنت نشط بدنيًا؟

`ativo`

- `0` — لا
- `1` — نعم

## إصدار الطريقة

Foster 1984 متعدد حدود بروس؛Bruce 1973 VO₂ بالعمر/النشاط؛MET=VO₂/3.5؛FAI

## المعادلة الموثقة

VO₂ (Foster, Bruce): 14.8 − 1.379 × t + 0.451 × t² − 0.012 × t³ (mL/kg/min; t بالدقائق)

METs = VO₂ ÷ 3.5

VO₂ المتوقع (Bruce): رجال خاملون 57.8 − 0.445 × العمر; نشطون 69.7 − 0.612 × العمر; نساء خاملات 42.3 − 0.356 × العمر; نشطات 42.9 − 0.312 × العمر

العجز الوظيفي (FAI) = (VO₂ المتوقع − المقاس) ÷ VO₂ المتوقع × 100

## الحدود والفئة السكانية

يجب أن يكون الزمن المستخدم لتقدير VO₂ من بروتوكول Bruce الموافق على جهاز المشي، لا مدة أي تمرين. تعطي المعادلة توقعًا، لا استهلاك أكسجين مقاسًا بتحليل الغازات. يستخدم MET القيمة الاصطلاحية ٣٫٥ mL/kg/min؛ ولا يقيس أيض الشخص في الراحة. مراجع القدرة المتوقعة والارتباطات الإنذارية خاصة بالسكان: درس Myers 2002 رجالًا محالين لاختبار سريري. لا تستقرئ تلقائيًا إلى الأطفال أو بروتوكولات أخرى أو خطر الوفاة الفردي.

## المراجع

- [Foster C et al. Generalized equations for predicting functional capacity from treadmill performance. Am Heart J, 1984.](https://doi.org/10.1016/0002-8703(84)90282-5)

- [Bruce RA, Kusumi F, Hosmer D. Maximal oxygen intake and nomographic assessment of functional aerobic impairment in cardiovascular disease. Am Heart J, 1973.](https://doi.org/10.1016/0002-8703(73)90502-4)

- [Myers J et al. Exercise capacity and mortality among men referred for exercise testing. N Engl J Med, 2002.](https://doi.org/10.1056/NEJMoa011858)

- [Foster1984](https://www.sciencedirect.com/science/article/pii/0002870384902825/pdf?md5=b82463125b785d7b4c7bb66e5b29bf38&pid=1-s2.0-0002870384902825-main.pdf)

## إعادة إجراء الاختبارات التقنية

شغّل node test.cjs في المجلد الجذري لهذا المستودع لتكرار الحالات الاصطناعية المسجلة. تُحفظ المدخلات والنتائج المتوقعة وحدود التفاوت الأصلية. لا تُعدّ الاختبارات التقنية تحققًا سريريًا.

```sh
node test.cjs
```

يحتوي tool.json على المصادر والإصدار ونطاق المراجعة. يحتفظ examples.json بالمدخلات والنتائج المتوقعة للحالات الاصطناعية؛ ويسجل results.json النتائج التي تم الحصول عليها.

[السجل والمراجع](../tool.json) · [شيفرة JavaScript](../calculator.js) · [حالات مرجعية](../examples.json) · [results.json](../results.json)

## المراجعة وشروط الاستخدام

لم تُجرَ مراجعة سريرية مستقلة.

هذه الواجهة ترجمة أعدّها مؤلفوها، وليست إصدارًا رسميًا أو معتمدًا. لم تُجرَ مراجعة سريرية مستقلة أو مراجعة لغوية مهنية، ولم تُستكمل الموافقة على حقوق استخدام الأدوات.

نتيجة المعادلة أو التصنيف. يعتمد التفسير والتصرف ومدى الانطباق على التقييم المهني والمصدر المحدد.

## الترخيص ونسبة العمل إلى أصحابه

ينطبق Apache-2.0 على كود ELUCENIA فقط. تبقى حقوق الأدوات والمنشورات والترجمات والبيانات لأصحابها المعنيين. احتفظ بملفّي LICENSE وNOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
