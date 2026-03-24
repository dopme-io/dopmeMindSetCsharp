# C# 7.3 — Roteiro MindSet

**Versão da linguagem:** 7.3  
**Contexto:** **maio de 2018**; dois temas — **código seguro** com desempenho próximo do **unsafe** (continuando **7.2**, com destaque para **`unmanaged`**) e **refinamentos** (tuplos com **`==`/`!=`**, variáveis de expressão, atributos em *backing field*, resolução de overload com **`in`**). Novas opções de compilador **`-publicsign`** e **`-pathmap`**.

Este roteiro usa o **SDK .NET atual** para exemplos. Inclui **cópia local** dos guias **7.2**, **7.1**, **7.0** e anteriores na mesma pasta. Não existe projeto MindSet **C# 6.0**; ver [csharp-7-0-overview.md](csharp-7-0-overview.md).

**Edição seguinte (C# 8.0):** [MindSetCSharp8_0.Console/Docs/README.md](../../MindSetCSharp8_0.Console/Docs/README.md) — .NET Core 3.0, NRT, `switch` expressions, `IAsyncEnumerable`, índices/ranges, …

**Edição seguinte (C# 9.0):** [MindSetCSharp9_0.Console/Docs/README.md](../../MindSetCSharp9_0.Console/Docs/README.md) — .NET 5, records, top-level statements, patterns relacionais, …

**Edição seguinte (C# 10.0):** [MindSetCSharp10_0.Console/Docs/README.md](../../MindSetCSharp10_0.Console/Docs/README.md) — .NET 6, *record structs*, `global using`, *handlers* de interpolação, …

## Documentos C# 7.3 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 7.3 | [csharp-7-3-overview.md](csharp-7-3-overview.md) |
| 1 | Restrição `where T : unmanaged` | [generic-constraint-unmanaged.md](generic-constraint-unmanaged.md) |
| 2 | Tema desempenho / código seguro (e 7.2) | [safe-code-performance-theme-7-3.md](safe-code-performance-theme-7-3.md) |
| 3 | `==` / `!=` em tuplos | [tuple-equality-operators.md](tuple-equality-operators.md) |
| 4 | Variáveis de expressão em mais sítios | [expression-variables-extended.md](expression-variables-extended.md) |
| 5 | `[field: …]` em propriedades autoimplementadas | [attribute-backing-field-auto-properties.md](attribute-backing-field-auto-properties.md) |
| 6 | Resolução de overload (`in`, menos ambiguidade) | [overload-resolution-improvements-7-3.md](overload-resolution-improvements-7-3.md) |
| 7 | `-publicsign`, `-pathmap` | [compiler-publicsign-pathmap.md](compiler-publicsign-pathmap.md) |

## Documentos C# 7.2 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 7.2 | [csharp-7-2-overview.md](csharp-7-2-overview.md) |
| 1 | Inicializadores `stackalloc` | [stackalloc-initializers.md](stackalloc-initializers.md) |
| 2 | `fixed` com *pattern* (ex.: Span) | [fixed-statements-pattern.md](fixed-statements-pattern.md) |
| 3 | Campos `fixed` sem *pinning* extra | [fixed-fields-without-pinning.md](fixed-fields-without-pinning.md) |
| 4 | Reatribuir `ref` locals | [ref-local-reassignment.md](ref-local-reassignment.md) |
| 5 | `readonly struct` | [readonly-struct.md](readonly-struct.md) |
| 6 | Parâmetros `in` | [in-parameter-modifier.md](in-parameter-modifier.md) |
| 7 | Retornos `ref readonly` | [ref-readonly-returns.md](ref-readonly-returns.md) |
| 8 | `ref struct` | [ref-struct.md](ref-struct.md) |
| 9 | Nota: restrições genéricas 7.2 / 7.3 | [generic-constraints-7-2-note.md](generic-constraints-7-2-note.md) |
| 10 | Argumentos nomeados não finais | [non-trailing-named-arguments.md](non-trailing-named-arguments.md) |
| 11 | `_` à esquerda em literais | [leading-underscores-numeric-literals.md](leading-underscores-numeric-literals.md) |
| 12 | `private protected` | [private-protected-access.md](private-protected-access.md) |
| 13 | Expressão condicional `ref` | [conditional-ref-expressions.md](conditional-ref-expressions.md) |

## Documentos C# 7.1 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 7.1 | [csharp-7-1-overview.md](csharp-7-1-overview.md) |
| 1 | `async` no `Main` | [async-main-method.md](async-main-method.md) |
| 2 | Literal `default` inferido | [default-literal.md](default-literal.md) |
| 3 | Nomes de tuplo inferidos | [inferred-tuple-element-names.md](inferred-tuple-element-names.md) |
| 4 | Pattern matching e `T` genérico | [pattern-matching-generic-type-parameters.md](pattern-matching-generic-type-parameters.md) |
| 5 | `LangVersion`, `-refout`, `-refonly` | [langversion-ref-assemblies.md](langversion-ref-assemblies.md) |

## Documentos C# 7.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral | [csharp-7-0-overview.md](csharp-7-0-overview.md) |
| 1 | Variáveis `out` inline | [out-variables.md](out-variables.md) |
| 2 | Tuplos e desconstrução | [tuples-deconstruction.md](tuples-deconstruction.md) |
| 3 | Pattern matching (início) | [pattern-matching.md](pattern-matching.md) |
| 4 | Funções locais | [local-functions.md](local-functions.md) |
| 5 | Membros com corpo de expressão (expandido) | [expression-bodied-members-expanded.md](expression-bodied-members-expanded.md) |
| 6 | `ref` locals e `ref` returns | [ref-locals-returns.md](ref-locals-returns.md) |
| 7 | Descartes (`_`) | [discards.md](discards.md) |
| 8 | Literais binários e separadores de dígitos | [binary-literals-digit-separators.md](binary-literals-digit-separators.md) |
| 9 | Expressões `throw` | [throw-expressions.md](throw-expressions.md) |

## Referência C# 5.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 5.0 | [csharp-5-0-overview.md](csharp-5-0-overview.md) |
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

1. Leia [csharp-7-3-overview.md](csharp-7-3-overview.md) e siga a tabela **C# 7.3**; use **7.2**/**7.1**/**7.0** conforme necessário.
2. Recorra às tabelas **5.0** … **1.0** quando precisar de fundações.
3. `dotnet run --project MindSetCSharp7_3.Console`

## Ligações

- Formato: [FORMATO_DO_PROJETO.md](../../FORMATO_DO_PROJETO.md)
- Índice: [DOCUMENTATION_INDEX.md](../../DOCUMENTATION_INDEX.md)
- Edição seguinte: [MindSetCSharp8_0.Console/Docs/README.md](../../MindSetCSharp8_0.Console/Docs/README.md) · [MindSetCSharp9_0.Console/Docs/README.md](../../MindSetCSharp9_0.Console/Docs/README.md) · [MindSetCSharp10_0.Console/Docs/README.md](../../MindSetCSharp10_0.Console/Docs/README.md)
- Edição anterior (C# 7.2): [MindSetCSharp7_2.Console/Docs/README.md](../../MindSetCSharp7_2.Console/Docs/README.md)
- Outras edições: [MindSetCSharp1_0.Console/Docs/README.md](../../MindSetCSharp1_0.Console/Docs/README.md) · [MindSetCSharp1_2.Console/Docs/README.md](../../MindSetCSharp1_2.Console/Docs/README.md) · [MindSetCSharp2_0.Console/Docs/README.md](../../MindSetCSharp2_0.Console/Docs/README.md) · [MindSetCSharp3_0.Console/Docs/README.md](../../MindSetCSharp3_0.Console/Docs/README.md) · [MindSetCSharp4_0.Console/Docs/README.md](../../MindSetCSharp4_0.Console/Docs/README.md) · [MindSetCSharp5_0.Console/Docs/README.md](../../MindSetCSharp5_0.Console/Docs/README.md) · [MindSetCSharp7_0.Console/Docs/README.md](../../MindSetCSharp7_0.Console/Docs/README.md) · [MindSetCSharp7_1.Console/Docs/README.md](../../MindSetCSharp7_1.Console/Docs/README.md) · [MindSetCSharp7_2.Console/Docs/README.md](../../MindSetCSharp7_2.Console/Docs/README.md)
