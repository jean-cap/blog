---
title: Verificar se é null
date: 2017-02-24 10:28:14
tags:
---
Em JavaScript, existem 5 tipos primitivos: `boolean`, `number`, `string`, `null` e `undefined`. Podemos verificar esses tipos utilizando o operador `typeof`, que retorna uma string com o tipo. Porém, no caso de `null`, o resultado é inesperado:

<!--more-->
```javascript
    console.log(typeof "Jean") // "string"
    console.log(typeof 10) // "number"
    console.log(typeof 5.1) // "number"
    console.log(typeof true) // "boolean"
    console.log(typeof undefined) // "undefined"

    console.log(typeof null) // "object"
```

A melhor maneira de verificar se um valor é `null` é compará-lo diretamente com `null`:

```javascript
    console.log(value === null) // true ou false
```