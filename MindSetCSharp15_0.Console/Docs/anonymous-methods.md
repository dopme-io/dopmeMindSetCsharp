# Métodos anónimos (C# 2.0)

## Contexto

**Métodos anónimos** permitem passar um **bloco de código** como **delegate** sem declarar um método nomeado separado. Sintaxe: `delegate (args) { ... }`.

Foram o passo imediato antes das **expressões lambda** (C# 3.0).

## O que implementar / praticar

1. Subscrever eventos com `delegate { ... }` ou `delegate(object s, EventArgs e) { ... }`.
2. Passar filtros para APIs que aceitam `Predicate<T>` ou delegates personalizados.

## Exemplo mínimo

```csharp
System.Threading.ThreadStart trabalho = delegate
{
    System.Console.WriteLine("A correr num delegate.");
};
```

Com parâmetros:

```csharp
var numeros = new System.Collections.Generic.List<int> { 1, 2, 3, 4 };
var pares = numeros.FindAll(delegate(int n) { return n % 2 == 0; });
```

## Mindset

- Encapsula **comportamento local** onde só é usado uma vez.
- Lambdas modernas (`n => n % 2 == 0`) são mais curtas; o modelo mental começa aqui.

## Próximo passo

[nullable-value-types.md](nullable-value-types.md)
