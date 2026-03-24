# Índices e intervalos (`Index`, `Range`) (C# 8.0)

## Ideia

Sintaxe **`^n`** (desde o fim) e **`start..end`** (intervalos) para **indexar** `Span`, `array`, ou tipos com **indexador** `Length`/`Count` compatível.

**Tipos de biblioteca:** `System.Index` e `System.Range` em **.NET Core 3.0+**.

## Exemplo

```csharp
var s = "abcdef";
var last = s[^1];
var slice = s[1..4];
```

## Mindset

- **Fatiamento** legível sem `Substring`/`Slice` verboso.

## Ver também

- [csharp-8-0-overview.md](csharp-8-0-overview.md)
