# `nameof` alargado (C# 11.0)

## Contexto

**`nameof`** pode referir-se a membros de tipos genéricos com **parâmetros de tipo** visíveis no contexto (ex.: `nameof(List<int>.Count)`), alargando cenários em atributos, mensagens e *logging* tipado.

## O que praticar

```csharp
_ = nameof(List<int>.Count); // "Count"
```

## Próximo passo

[nint-nuint-inptr-aliases.md](nint-nuint-inptr-aliases.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
