# `params` em coleções (C# 13.0)

## Contexto

O modificador **`params`** deixa de estar limitado a **arrays**. Pode usar-se com tipos de coleção reconhecidos pelo compilador, incluindo **`Span<T>`**, **`ReadOnlySpan<T>`**, **`IEnumerable<T>`** e outras interfaces/coleções suportadas.

## O que praticar

```csharp
static void M(params ReadOnlySpan<int> values) { }

M(1, 2, 3);
```

Relacione com [indices-and-ranges.md](indices-and-ranges.md) (C# 8) e coleções em [collection-expressions.md](collection-expressions.md) (C# 12).

## Próximo passo

[lock-system-threading-lock.md](lock-system-threading-lock.md) · [csharp-13-0-overview.md](csharp-13-0-overview.md)
