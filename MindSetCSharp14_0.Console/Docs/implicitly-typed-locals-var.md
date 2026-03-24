# Variáveis locais com tipo implícito — `var` (C# 3.0)

## Contexto

Em **C# 3.0**, **`var`** permite declarar uma variável local cujo **tipo é inferido pelo compilador** a partir da expressão à direita. O tipo continua a ser **estático** em tempo de compilação — **não** é `dynamic` nem “tipo desconhecido”.

## O que praticar

1. `var s = "texto";` — o compilador infere `string`.
2. `var xs = new List<int> { 1, 2, 3 };` — combina bem com [object-collection-initializers.md](object-collection-initializers.md).
3. Evitar `var` quando a expressão à direita **não** deixa o tipo óbvio para quem lê o código.

## Exemplo mínimo

```csharp
using System.Linq;

var numeros = new[] { 1, 2, 3, 4, 5 };
var pares = numeros.Where(n => n % 2 == 0);
```

(`Where` requer `using System.Linq;` — método de extensão; ver [extension-methods.md](extension-methods.md) e [lambda-expressions.md](lambda-expressions.md).)

## Mindset

`var` reduz repetição de nomes de tipo longos; a legibilidade depende do **nome das variáveis** e da clareza do lado direito.

## Próximo passo

[auto-implemented-properties.md](auto-implemented-properties.md)
