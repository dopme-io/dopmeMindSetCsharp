# Novas linhas em interpolação (C# 11.0)

## Contexto

Dentro de **`$"…{ … }…"`** (e *raw* interpoladas), a expressão entre **`{` e `}`** pode ocupar **várias linhas**, o que melhora a legibilidade de expressões longas.

## O que praticar

```csharp
var s = $"resultado: {
    Math.Sqrt(2) + 1
}";
```

## Próximo passo

[interpolated-string-handlers.md](interpolated-string-handlers.md) (C# 10) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
