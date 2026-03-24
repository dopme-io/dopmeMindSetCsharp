# Operadores de atribuição composta definidos pelo utilizador (C# 14.0)

## Contexto

Tipos podem definir **`operator +=`**, **`-=`**, e outros **operadores de atribuição composta** com semântica personalizada — o compilador usa-os em expressões como **`x += y`**.

## O que praticar

```csharp
public static Thing operator +=(Thing a, Thing b) => a.Combine(b);
```

Relacione com [operators-and-expressions.md](operators-and-expressions.md) (base).

## Próximo passo

[csharp-13-0-overview.md](csharp-13-0-overview.md) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
