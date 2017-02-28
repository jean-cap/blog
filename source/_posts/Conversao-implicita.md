---
title: Conversão implícita
date: 2017-02-21 10:23:38
tags:
---
Uma pegadinha do JavaScript que geralmente pega de surpresa quem está iniciando na linguagem é a conversão implícita de tipos. Isto acontece geralmente em comparações em estruturas de controle, tal como um `if`.

<!--more-->
Observe o código a seguir:

```javascript
    console.log("5" == 5) // true
    console.log("5" === 5) // false

    console.log(undefined == null) // true
    console.log(undefined === null) // false
```

Na primeira linha, a igualdade dupla é utilizada e o JavaScript converte implicitamente a `string` “5” para um inteiro e então faz a comparação, o resultado é `true`. Já na segunda linha, quando utilizamos o operador de igualdade tripla `===`, a conversão não ocorre, então é recomendado utilizar sempre este operador para uma maior segurança no código. Da mesma forma, quando quando comparamos `undefined` e `null`, a igualdade dupla mostra que eles são equivalentes, enquanto a igualdade tripla diz que não.

Para saber como o JavaScript realiza as conversões com seus respectivos tipos, dê uma olhada [nesta tabela](https://dorey.github.io/JavaScript-Equality-Table/ "Tabela de conversões de tipos do JavaScript." target="_blank").