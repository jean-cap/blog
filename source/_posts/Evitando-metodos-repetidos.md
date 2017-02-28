---
title: Evitando métodos repetidos
date: 2017-02-28 09:19:31
tags:
---
Ao criar um tipo de objeto, não coloque os métodos no próprio construtor, coloque-o eu seu `prototype` para que este seja compartilhado por todas as instâncias. Veja o código abaixo:
<!--more-->
```javascript
    function Pessoa(nome) {
        this.nome = nome;
        this.imprimeNome = function () {
            console.log(this.nome);
        }
    }

    var pessoa1 = new Pessoa('Jean');
    pessoa1.imprimeNome(); // Jean

    var pessoa2 = new Pessoa('Bruno');
    pessoa2.imprimeNome(); // Bruno
```

No exemplo acima, cada instância do construtor `Pessoa`, terá seu próprio método `imprimeNome()`, ao invés disso, seria melhor ter um único método, compartilhado entre todas as instâncias. Veja o código abaixo:

```javascript
    function Pessoa(nome) {
        this.nome = nome;
    }
    Pessoa.prototype.imprimeNome = function () {
        console.log(this.nome);
    };

    var pessoa1 = new Pessoa('Jean');
    pessoa1.imprimeNome(); // Jean

    var pessoa2 = new Pessoa('Bruno');
    pessoa2.imprimeNome(); // Bruno
```

Isso também tem outra vantagem, qualquer mudança no método `imprimeNome()` será refletida em todas as instâncias, mesmo que o objeto já tenha sido instanciado.