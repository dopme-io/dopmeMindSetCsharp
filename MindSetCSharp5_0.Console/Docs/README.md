# C# 5.0 — Roteiro MindSet

**Versão da linguagem:** 5.0  
**Contexto:** **agosto de 2012**, com o **Visual Studio 2012** e o **.NET Framework 4.5**. A versão foi **muito focada**: o protagonista é **`async`** / **`await`**, que tornaram a **assincronia** um conceito de **primeira classe** na linguagem, reduzindo o encadeamento manual de tarefas e callbacks. Em paralelo, os **atributos de informação do chamador** simplificam **logging** e **diagnóstico** sem reflexão repetitiva.

Este roteiro usa o **SDK .NET atual** para exemplos; os textos assinalam o que é próprio de **5.0** e o que são evoluções posteriores.

## Documentos C# 5.0 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral | [csharp-5-0-overview.md](csharp-5-0-overview.md) |
| 1 | Membros assíncronos (`async` / `await`) | [async-await.md](async-await.md) |
| 2 | Atributos de informação do chamador | [caller-info-attributes.md](caller-info-attributes.md) |

## Referência C# 4.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 4.0 | [csharp-4-0-overview.md](csharp-4-0-overview.md) |
| 1 | Ligação dinâmica (`dynamic`) | [dynamic-binding.md](dynamic-binding.md) |
| 2 | Argumentos nomeados e parâmetros opcionais | [named-optional-arguments.md](named-optional-arguments.md) |
| 3 | Variança `out` / `in` em interfaces genéricas | [generic-variance-interfaces.md](generic-variance-interfaces.md) |
| 4 | Tipos de interop incorporados (NoPIA) | [embedded-interop-types.md](embedded-interop-types.md) |

## Referência C# 3.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 3.0 | [csharp-3-0-overview.md](csharp-3-0-overview.md) |
| 1 | Variáveis locais com tipo implícito (`var`) | [implicitly-typed-locals-var.md](implicitly-typed-locals-var.md) |
| 2 | Propriedades autoimplementadas | [auto-implemented-properties.md](auto-implemented-properties.md) |
| 3 | Inicializadores de objeto e de coleção | [object-collection-initializers.md](object-collection-initializers.md) |
| 4 | Tipos anónimos | [anonymous-types.md](anonymous-types.md) |
| 5 | Expressões lambda | [lambda-expressions.md](lambda-expressions.md) |
| 6 | Métodos de extensão | [extension-methods.md](extension-methods.md) |
| 7 | Expressões de consulta e LINQ | [query-expressions-linq.md](query-expressions-linq.md) |
| 8 | Árvores de expressão | [expression-trees.md](expression-trees.md) |
| 9 | Métodos parciais | [partial-methods.md](partial-methods.md) |

## Referência C# 2.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 2.0 | [csharp-2-0-overview.md](csharp-2-0-overview.md) |
| 1 | Genéricos | [generics.md](generics.md) |
| 2 | Tipos parciais | [partial-types.md](partial-types.md) |
| 3 | Métodos anónimos | [anonymous-methods.md](anonymous-methods.md) |
| 4 | Nullable | [nullable-value-types.md](nullable-value-types.md) |
| 5 | Iteradores | [iterators.md](iterators.md) |
| 6 | Covariância / contravariância (delegados; enquadramento) | [covariance-contravariance.md](covariance-contravariance.md) |
| 7 | Outras melhorias 2.0 | [other-features-2-0.md](other-features-2-0.md) |

## Base C# 1.0 (referência na mesma pasta)

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

1. Leia [csharp-5-0-overview.md](csharp-5-0-overview.md) e siga a tabela **C# 5.0**.
2. Recorra às tabelas **4.0**, **3.0**, **2.0** e **1.0** quando precisar de fundações.
3. `dotnet run --project MindSetCSharp5_0.Console`

## Ligações

- Formato: [FORMATO_DO_PROJETO.md](../../FORMATO_DO_PROJETO.md)
- Índice: [DOCUMENTATION_INDEX.md](../../DOCUMENTATION_INDEX.md)
- Edições anteriores: [MindSetCSharp1_0.Console/Docs/README.md](../../MindSetCSharp1_0.Console/Docs/README.md) · [MindSetCSharp1_2.Console/Docs/README.md](../../MindSetCSharp1_2.Console/Docs/README.md) · [MindSetCSharp2_0.Console/Docs/README.md](../../MindSetCSharp2_0.Console/Docs/README.md) · [MindSetCSharp3_0.Console/Docs/README.md](../../MindSetCSharp3_0.Console/Docs/README.md) · [MindSetCSharp4_0.Console/Docs/README.md](../../MindSetCSharp4_0.Console/Docs/README.md)
- Edição seguinte (C# 7.0): [MindSetCSharp7_0.Console/Docs/README.md](../../MindSetCSharp7_0.Console/Docs/README.md) *(não há projeto MindSet C# 6.0 no repositório)* · [C# 7.1](../../MindSetCSharp7_1.Console/Docs/README.md) · [C# 7.2](../../MindSetCSharp7_2.Console/Docs/README.md) · [C# 7.3](../../MindSetCSharp7_3.Console/Docs/README.md) · [C# 8.0](../../MindSetCSharp8_0.Console/Docs/README.md) · [C# 9.0](../../MindSetCSharp9_0.Console/Docs/README.md) · [C# 10.0](../../MindSetCSharp10_0.Console/Docs/README.md)
