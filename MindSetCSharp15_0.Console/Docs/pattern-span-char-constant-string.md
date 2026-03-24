# Pattern com `Span<char>` / literal constante (C# 11.0)

## Contexto

Em **pattern matching**, pode comparar **`ReadOnlySpan<char>`** ou **`Span<char>`** com uma **string constante** (ex.: em `switch`), útil para APIs baseadas em *span* sem alocar `string`.

## O que praticar

```csharp
static bool IsHi(ReadOnlySpan<char> s) => s is "hi";
```

## Próximo passo

[extended-nameof.md](extended-nameof.md) · [pattern-matching.md](pattern-matching.md) (C# 7) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
