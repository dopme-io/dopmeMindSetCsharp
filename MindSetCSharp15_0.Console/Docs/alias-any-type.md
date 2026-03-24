# Alias para qualquer tipo (`using`) (C# 12.0)

## Contexto

A diretiva **`using X = …`** pode aliasar **qualquer tipo**, incluindo **tuplos**, **ponteiros**, tipos com **parâmetros de tipo aninhados**, etc. — não só *named types* simples.

## O que praticar

```csharp
using IntPair = (int A, int B);
```

## Próximo passo

[experimental-attribute.md](experimental-attribute.md) · [csharp-12-0-overview.md](csharp-12-0-overview.md)
