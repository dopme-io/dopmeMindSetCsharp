# `nameof` com genéricos não ligados (C# 14.0)

## Contexto

**`nameof`** aceita **tipos genéricos sem argumentos de tipo** (*unbound generic types*), por exemplo **`nameof(List<>)`**, útil em atributos, mensagens e metadados sem fixar `T`.

## O que praticar

```csharp
_ = nameof(Dictionary<,>);
```

Relacione com [extended-nameof.md](extended-nameof.md) (C# 11).

## Próximo passo

[span-implicit-conversions.md](span-implicit-conversions.md) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
