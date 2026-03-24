# C# 11.0 — Roteiro MindSet

**Versão da linguagem:** 11.0  
**Contexto:** **novembro de 2022**; alinhado a **.NET 7** e à **cadência anual** de releases. Matemática genérica (`INumber<T>`, …), *raw string literals*, literais UTF-8, *list patterns*, tipos `file`, membros `required`, `ref fields` / `scoped`, e refinamentos em patterns e conversões.

Este roteiro usa o **SDK .NET atual** para exemplos. O `.csproj` fixa **`LangVersion` 11**. Inclui **cópia local** dos guias **10.0** e anteriores na mesma pasta. Não existe projeto MindSet **C# 6.0**; ver [csharp-7-0-overview.md](csharp-7-0-overview.md).

## Documentos C# 11.0 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 11.0 | [csharp-11-0-overview.md](csharp-11-0-overview.md) |
| 1 | *Raw string literals* | [raw-string-literals.md](raw-string-literals.md) |
| 2 | Matemática genérica | [generic-math.md](generic-math.md) |
| 3 | Atributos genéricos | [generic-attributes.md](generic-attributes.md) |
| 4 | Literais UTF-8 | [utf8-string-literals.md](utf8-string-literals.md) |
| 5 | Novas linhas em interpolação | [interpolated-newlines.md](interpolated-newlines.md) |
| 6 | *List patterns* | [list-patterns.md](list-patterns.md) |
| 7 | Tipos `file` | [file-local-types.md](file-local-types.md) |
| 8 | Membros `required` | [required-members.md](required-members.md) |
| 9 | *Auto-default structs* | [auto-default-structs.md](auto-default-structs.md) |
| 10 | Pattern `Span<char>` / literal | [pattern-span-char-constant-string.md](pattern-span-char-constant-string.md) |
| 11 | `nameof` alargado | [extended-nameof.md](extended-nameof.md) |
| 12 | `nint` / `nuint` e `IntPtr` / `UIntPtr` | [nint-nuint-inptr-aliases.md](nint-nuint-inptr-aliases.md) |
| 13 | `ref fields` / `scoped ref` | [ref-fields-scoped-ref.md](ref-fields-scoped-ref.md) |
| 14 | *Method group* → delegado | [method-group-delegate-improved.md](method-group-delegate-improved.md) |
| 15 | *Warning wave* 7 | [warning-wave-7.md](warning-wave-7.md) |

## Documentos C# 10.0 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 10.0 | [csharp-10-0-overview.md](csharp-10-0-overview.md) |
| 1 | *Record structs* | [record-structs.md](record-structs.md) |
| 2 | Melhorias em tipos estrutura | [structure-types-improvements.md](structure-types-improvements.md) |
| 3 | *Handlers* de strings interpoladas | [interpolated-string-handlers.md](interpolated-string-handlers.md) |
| 4 | `global using` | [global-usings.md](global-usings.md) |
| 5 | `namespace` ao âmbito do ficheiro | [file-scoped-namespace.md](file-scoped-namespace.md) |
| 6 | *Property patterns* alargados | [extended-property-patterns.md](extended-property-patterns.md) |
| 7 | Tipo natural da lambda | [lambda-natural-type.md](lambda-natural-type.md) |
| 8 | Tipo de retorno explícito (lambda) | [lambda-explicit-return-type.md](lambda-explicit-return-type.md) |
| 9 | Atributos em lambdas | [attributes-on-lambda-expressions.md](attributes-on-lambda-expressions.md) |
| 10 | `const string` + interpolação | [const-string-interpolation.md](const-string-interpolation.md) |
| 11 | `sealed` em `ToString` de *record* | [record-tostring-sealed.md](record-tostring-sealed.md) |
| 12 | Análise nulo / atribuição definida | [null-analysis-improvements.md](null-analysis-improvements.md) |
| 13 | Desconstrução mista | [deconstruction-assignment-declaration.md](deconstruction-assignment-declaration.md) |
| 14 | `[AsyncMethodBuilder]` em métodos | [async-method-builder-attribute.md](async-method-builder-attribute.md) |
| 15 | `[CallerArgumentExpression]` | [caller-argument-expression.md](caller-argument-expression.md) |
| 16 | Pragma `#line` (novo formato) | [line-pragma-csharp-10.md](line-pragma-csharp-10.md) |
| 17 | *Preview* (C# 10) | [preview-features-csharp-10.md](preview-features-csharp-10.md) |

## Documentos C# 9.0 (ordem sugerida)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 9.0 | [csharp-9-0-overview.md](csharp-9-0-overview.md) |
| 1 | *Records* | [records.md](records.md) |
| 2 | *Setters* só `init` | [init-only-setters.md](init-only-setters.md) |
| 3 | Instruções de nível superior | [top-level-statements.md](top-level-statements.md) |
| 4 | Patterns relacionais e lógicos | [pattern-relational-logical.md](pattern-relational-logical.md) |
| 5 | `nint` / `nuint` | [native-sized-integers.md](native-sized-integers.md) |
| 6 | Ponteiros de função | [function-pointers.md](function-pointers.md) |
| 7 | Omitir `localsinit` | [skip-localsinit.md](skip-localsinit.md) |
| 8 | Inicializadores de módulo | [module-initializers.md](module-initializers.md) |
| 9 | Métodos parciais (regras novas) | [partial-methods-csharp-9.md](partial-methods-csharp-9.md) |
| 10 | `new` com tipo alvo | [target-typed-new.md](target-typed-new.md) |
| 11 | Lambdas `static` | [static-anonymous-functions.md](static-anonymous-functions.md) |
| 12 | `?:` com tipo alvo | [target-typed-conditional.md](target-typed-conditional.md) |
| 13 | Retornos covariantes | [covariant-return-types.md](covariant-return-types.md) |
| 14 | `GetEnumerator` de extensão + `foreach` | [extension-getenumerator-foreach.md](extension-getenumerator-foreach.md) |
| 15 | Descartes em lambdas | [lambda-discard-parameters.md](lambda-discard-parameters.md) |
| 16 | Atributos em funções locais | [attributes-local-functions.md](attributes-local-functions.md) |

## Documentos C# 8.0 (ficheiros na mesma pasta)

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | Visão geral 8.0 | [csharp-8-0-overview.md](csharp-8-0-overview.md) |
| 1 | Membros `readonly` | [readonly-members.md](readonly-members.md) |
| 2 | Membros predefinidos de interface | [default-interface-members.md](default-interface-members.md) |
| 3 | Expressões `switch` | [pattern-switch-expressions.md](pattern-switch-expressions.md) |
| 4 | *Property patterns* | [pattern-property-patterns.md](pattern-property-patterns.md) |
| 5 | *Tuple patterns* | [pattern-tuple-patterns.md](pattern-tuple-patterns.md) |
| 6 | *Positional patterns* | [pattern-positional-patterns.md](pattern-positional-patterns.md) |
| 7 | Declarações `using` | [using-declarations.md](using-declarations.md) |
| 8 | Funções locais `static` | [static-local-functions.md](static-local-functions.md) |
| 9 | `ref struct` descartável | [disposable-ref-structs.md](disposable-ref-structs.md) |
| 10 | Tipos de referência anuláveis | [nullable-reference-types.md](nullable-reference-types.md) |
| 11 | Fluxos assíncronos | [asynchronous-streams.md](asynchronous-streams.md) |
| 12 | Índices e intervalos | [indices-and-ranges.md](indices-and-ranges.md) |
| 13 | `??=` | [null-coalescing-assignment.md](null-coalescing-assignment.md) |
| 14 | Tipos construídos `unmanaged` | [unmanaged-constructed-types.md](unmanaged-constructed-types.md) |
| 15 | `stackalloc` aninhado | [stackalloc-nested-expressions.md](stackalloc-nested-expressions.md) |
| 16 | Interpolação + verbatim | [interpolated-verbatim-strings-8-0.md](interpolated-verbatim-strings-8-0.md) |

## Documentos C# 7.3 (ficheiros na mesma pasta)

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

1. Leia [csharp-11-0-overview.md](csharp-11-0-overview.md) e siga a tabela **C# 11.0**; use **10.0** / **9.0** / **8.0** conforme necessário.
2. Recorra às tabelas **5.0** … **1.0** quando precisar de fundações.
3. `dotnet run --project MindSetCSharp11_0.Console`

## Ligações

- Formato: [FORMATO_DO_PROJETO.md](../../FORMATO_DO_PROJETO.md)
- Índice: [DOCUMENTATION_INDEX.md](../../DOCUMENTATION_INDEX.md)
- Edição anterior (C# 10.0): [MindSetCSharp10_0.Console/Docs/README.md](../../MindSetCSharp10_0.Console/Docs/README.md)
- Edição seguinte (C# 12.0): [MindSetCSharp12_0.Console/Docs/README.md](../../MindSetCSharp12_0.Console/Docs/README.md)
- Edição seguinte (C# 13.0): [MindSetCSharp13_0.Console/Docs/README.md](../../MindSetCSharp13_0.Console/Docs/README.md)
- Edição seguinte (C# 14.0): [MindSetCSharp14_0.Console/Docs/README.md](../../MindSetCSharp14_0.Console/Docs/README.md)
- Edição seguinte (C# 15.0): [MindSetCSharp15_0.Console/Docs/README.md](../../MindSetCSharp15_0.Console/Docs/README.md)
- Outras edições: [MindSetCSharp1_0.Console/Docs/README.md](../../MindSetCSharp1_0.Console/Docs/README.md) · [MindSetCSharp1_2.Console/Docs/README.md](../../MindSetCSharp1_2.Console/Docs/README.md) · [MindSetCSharp2_0.Console/Docs/README.md](../../MindSetCSharp2_0.Console/Docs/README.md) · [MindSetCSharp3_0.Console/Docs/README.md](../../MindSetCSharp3_0.Console/Docs/README.md) · [MindSetCSharp4_0.Console/Docs/README.md](../../MindSetCSharp4_0.Console/Docs/README.md) · [MindSetCSharp5_0.Console/Docs/README.md](../../MindSetCSharp5_0.Console/Docs/README.md) · [MindSetCSharp7_0.Console/Docs/README.md](../../MindSetCSharp7_0.Console/Docs/README.md) · [MindSetCSharp7_1.Console/Docs/README.md](../../MindSetCSharp7_1.Console/Docs/README.md) · [MindSetCSharp7_2.Console/Docs/README.md](../../MindSetCSharp7_2.Console/Docs/README.md) · [MindSetCSharp7_3.Console/Docs/README.md](../../MindSetCSharp7_3.Console/Docs/README.md) · [MindSetCSharp8_0.Console/Docs/README.md](../../MindSetCSharp8_0.Console/Docs/README.md) · [MindSetCSharp9_0.Console/Docs/README.md](../../MindSetCSharp9_0.Console/Docs/README.md)
