---
title: Verificar se é NaN
date: 2017-02-24 09:06:47
tags:
---
Em JavaScript, NaN não é comparável a qualquer outro valor, isso significa que não é possível realizar teste de igualdade do tipo <!--more--> `x == NaN`, em vez disso, deve escrever `x != x`.
Essa expressão será verdadeira se, e somente se, `x` for `NaN`. Para verificar se o valor não é um número, pode-se utilizar a função `isNaN(x)` que retorna `true` se o valor não for um número.

```javascript
    var testeNan = 5 - 'a';
    console.log(testeNan); // NaN
    console.log(testeNan != testeNan); // true
    console.log(testeNan !== testeNan); // true
    console.log(isNaN(testeNan)); // true
```