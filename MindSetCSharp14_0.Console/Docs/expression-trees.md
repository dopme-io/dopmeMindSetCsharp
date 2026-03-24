# Árvores de expressão (C# 3.0)

## Contexto

Uma **árvore de expressão** (`System.Linq.Expressions.Expression<TDelegate>`) é uma **representação em dados** de uma expressão lambda — nós descrevem chamadas, operadores, parâmetros, etc. O compilador **pode** gerar essa árvore quando o tipo alvo é `Expression<…>` em vez de um delegado “executável” normal.

Isto permitiu a **LINQ** remoto (ex.: traduzir uma expressão para **SQL**) porque a consulta pode ser **inspecionada em tempo de execução**, não só invocada como IL.

## O que praticar

1. Comparar:
   - `Func<int, bool> f = x => x > 0;` — delegado, invocável.
   - `Expression<Func<int, bool>> e = x => x > 0;` — árvore, analisável (`e.Body`, `e.Parameters`, …).
2. **Nem** toda lambda pode virar árvore: corpos com blocos `{}` ou instruções arbitrárias **não** são suportados na forma de árvore (só certas expressões).

## Exemplo mínimo

```csharp
using System.Linq.Expressions;

Expression<Func<int, bool>> maiorQueZero = x => x > 0;
// Inspecionar maiorQueZero.Body em depuração
```

## Mindset

**Código como dado**: útil para frameworks (ORM, pipelines); custo mental extra face a um delegado simples.

## Próximo passo

[partial-methods.md](partial-methods.md)
