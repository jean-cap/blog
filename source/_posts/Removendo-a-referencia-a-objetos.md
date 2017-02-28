---
title: Removendo a referência a objetos
date: 2017-02-24 11:21:39
tags:
---
O JavaScript possui garbage-collection (coleta de lixo), portanto não é realmente necessário se preocupar com alocações de memória ao usar tipos de referência (objetos).
<!--more-->
Entretanto é melhor remover a referência aos objetos que não sejam mais necessários para que o coletor de lixo possa liberar esta memória. A melhor forma de fazer isso é atribuir `null` a variável do objeto:

```javascript
    var object = new Object();
    // faça algo
    object = null;
```

Nesse caso, `object` é criado e usado antes de finalmente ser definido como `null`. Remover a referência aos objetos é especialmente importante em aplicações grandes.