# Expressões de coleção (C# 12.0)

## Contexto

Nova sintaxe **`[ … ]`** para construir coleções de forma **uniforme** (listas, *spans*, tipos alvo). O operador ***spread*** **`..expr`** expande outra coleção no meio da expressão.

## O que praticar

```csharp
int[] a = [1, 2, 3];
int[] b = [0, ..a, 4];
List<string> names = ["a", "b"];
```

Relacione com inicializadores em [object-collection-initializers.md](object-collection-initializers.md) (C# 3).

## Próximo passo

[inline-arrays.md](inline-arrays.md) · [csharp-12-0-overview.md](csharp-12-0-overview.md)
