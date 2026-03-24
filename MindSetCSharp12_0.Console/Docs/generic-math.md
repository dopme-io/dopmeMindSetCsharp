# Matemática genérica (C# 11.0)

## Contexto

Interfaces numéricas em **`System.Numerics`** (ex.: **`INumber<TSelf>`**), **operadores estáticos abstratos** e **restrições `where T : INumber<T>`** permitem escrever **um algoritmo** que funciona com `int`, `double`, `decimal`, etc., sem duplicar código.

## O que praticar

```csharp
static T Sum<T>(ReadOnlySpan<T> values) where T : INumber<T>
{
    T total = T.Zero;
    foreach (var v in values)
        total += v;
    return total;
}
```

## Próximo passo

[generic-attributes.md](generic-attributes.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
