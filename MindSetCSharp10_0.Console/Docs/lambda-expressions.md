# Expressões lambda (C# 3.0)

## Contexto

As **lambdas** compactam delegados: em vez de `delegate(int x) { return x * 2; }` (C# 2.0, ver [anonymous-methods.md](anonymous-methods.md)), usa-se **`x => x * 2`**.

Lambdas com corpo de **expressão** são atribuíveis a `Func<…>` / `Action<…>`. Quando o contexto espera **`Expression<TDelegate>`**, o compilador pode gerar uma **árvore de expressão** em vez de IL direto — ver [expression-trees.md](expression-trees.md).

## O que praticar

1. `Func<int, int> dobro = x => x * 2;`
2. `numeros.Where(n => n > 0)` com LINQ.
3. Lambdas que capturam variáveis locais (**closure**) — entender ciclo de vida e efeitos colaterais.

## Exemplo mínimo

```csharp
using System.Linq;

int[] vals = { 1, 2, 3, 4 };
var somaPares = vals.Where(n => n % 2 == 0).Sum();
```

## Mindset

Menos cerimónia que métodos anónimos; a legibilidade pede **nomes** claros quando a lambda cresce — aí um **método nomeado** pode ser melhor.

## Próximo passo

[extension-methods.md](extension-methods.md)
