# C# 2.0 — Roteiro MindSet

**Versão da linguagem:** 2.0  
**Contexto:** **novembro de 2005**, com o **Visual Studio 2005** e **.NET 2.0**. C# passou a suportar **genéricos** em tipos e métodos, **iteradores** (`yield`), **tipos parciais**, **métodos anónimos**, **nullable** para tipos valor, refinamentos em **delegados** e mais.

Este roteiro usa o **SDK .NET atual** para exemplos; os textos assinalam o que é próprio de **2.0** e o que são evoluções posteriores.

## Documentos C# 2.0 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral | [csharp-2-0-overview.md](csharp-2-0-overview.md) |
| 1 | Genéricos | [generics.md](generics.md) |
| 2 | Tipos parciais | [partial-types.md](partial-types.md) |
| 3 | Métodos anónimos | [anonymous-methods.md](anonymous-methods.md) |
| 4 | Tipos valor anuláveis (`Nullable<T>`, `int?`) | [nullable-value-types.md](nullable-value-types.md) |
| 5 | Iteradores (`yield`) | [iterators.md](iterators.md) |
| 6 | Covariância / contravariância (enquadramento 2.0) | [covariance-contravariance.md](covariance-contravariance.md) |
| 7 | Outras melhorias (get/set, static class, grupo de métodos, …) | [other-features-2-0.md](other-features-2-0.md) |

## Base C# 1.0 (referência na mesma pasta)

Os ficheiros abaixo repetem o enquadramento da edição **MindSet C# 1.0** para consulta rápida.

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 1 | Classes | [classes.md](classes.md) |
| 2 | Structs | [structs.md](structs.md) |
| 3 | Interfaces | [interfaces.md](interfaces.md) |
| 4 | Eventos | [events.md](events.md) |
| 5 | Propriedades | [properties.md](properties.md) |
| 6 | Delegates | [delegates.md](delegates.md) |
| 7 | Operadores e expressões | [operators-and-expressions.md](operators-and-expressions.md) |
| 8 | Instruções (statements) | [statements.md](statements.md) |
| 9 | Atributos | [attributes.md](attributes.md) |

## Como usar

1. Leia [csharp-2-0-overview.md](csharp-2-0-overview.md) e siga a tabela **C# 2.0**.
2. Use a base 1.0 conforme precisar.
3. `dotnet run --project MindSetCSharp2_0.Console`

## Ligações

- Formato: [FORMATO_DO_PROJETO.md](../../FORMATO_DO_PROJETO.md)
- Índice: [DOCUMENTATION_INDEX.md](../../DOCUMENTATION_INDEX.md)
- Edições anteriores: [MindSetCSharp1_0.Console/Docs/README.md](../../MindSetCSharp1_0.Console/Docs/README.md) · [MindSetCSharp1_2.Console/Docs/README.md](../../MindSetCSharp1_2.Console/Docs/README.md)
- Edições seguintes: [C# 3.0](../../MindSetCSharp3_0.Console/Docs/README.md) (LINQ, lambdas, `var`, …) · [C# 4.0](../../MindSetCSharp4_0.Console/Docs/README.md) (`dynamic`, `out`/`in`, NoPIA, …) · [C# 5.0](../../MindSetCSharp5_0.Console/Docs/README.md) (`async`/`await`, caller info, …) · [C# 7.0](../../MindSetCSharp7_0.Console/Docs/README.md) (tuplos, `out var`, patterns, …) · [C# 7.1](../../MindSetCSharp7_1.Console/Docs/README.md) (`async Main`, `default`, …) · [C# 7.2](../../MindSetCSharp7_2.Console/Docs/README.md) (`in`, `ref struct`, …) · [C# 7.3](../../MindSetCSharp7_3.Console/Docs/README.md) (`unmanaged`, tuplos `==`, …) · [C# 8.0](../../MindSetCSharp8_0.Console/Docs/README.md) (NRT, `IAsyncEnumerable`, …) · [C# 9.0](../../MindSetCSharp9_0.Console/Docs/README.md) (records, top-level statements, …) · [C# 10.0](../../MindSetCSharp10_0.Console/Docs/README.md) (*record structs*, .NET 6, …)
