---
title: Diferença entre pré incremento e pós incremento
date: 2017-02-22 09:02:49
tags:
---
Hoje trago uma dica rápida e simples mas que muita gente não conhece sobre a diferença entre pré incremento/decremento e pós incremento/decremento. É muito importante saber a diferença para evitar comportamentos indesejados. Veja o código a seguir:

<!--more-->
```javascript
    // RETORNA 0, POIS PRIMEIRO RETORNA E DEPOIS REALIZA A OPERAÇÃO DE ADIÇÃO
    function minhaFuncao1() {
        var exemplo = 0;
        return exemplo++;
    }
    console.log(minhaFuncao1()); // 0

    // RETORNA 1, POIS PRIMEIRO REALIZA A OPERAÇÃO DE ADIÇÃO E DEPOIS RETORNA
    function minhaFuncao2() {
        var exemplo = 0;
        return ++exemplo;
    }
    console.log(minhaFuncao2()); // 1
```

Até a próxima!