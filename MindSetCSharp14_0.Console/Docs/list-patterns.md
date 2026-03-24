# *List patterns* (C# 11.0)

## Contexto

Patterns aplicam-se a **sequências indexáveis** (`array`, `List<T>`, *span*, …): combinar **elementos**, **`..` (*slice*)** e comprimento, por exemplo **`[1, 2, ..]`**, **`[var first, .., var last]`**.

## O que praticar

```csharp
static string Describe(int[] xs) => xs switch
{
    [] => "vazio",
    [var x] => $"um: {x}",
    [var a, var b, ..] => $"dois+: {a},{b},…",
    _ => "outro"
};
```

Relacione com [extended-property-patterns.md](extended-property-patterns.md) (C# 10) e patterns em [pattern-switch-expressions.md](pattern-switch-expressions.md).

## Próximo passo

[file-local-types.md](file-local-types.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
