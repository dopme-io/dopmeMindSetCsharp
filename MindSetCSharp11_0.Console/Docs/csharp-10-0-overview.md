# C# 10.0 — visão geral (novembro 2021)

## Contexto

**C# 10.0** acompanha **.NET 6** e reforça a **cadência anual** de releases do .NET. Continua os temas: **menos cerimónia**, **dados vs algoritmos** e **desempenho** (runtime). Vários recursos foram aplicados no próprio **.NET Runtime** para ganhos com **interpolated string handlers** e **`AsyncMethodBuilder`**.

Algumas capacidades chegaram como **pré-visualização** em C# 10 (podem mudar antes do estado final): **atributos genéricos** e **membros estáticos abstratos em interfaces**.

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| *Record structs* | [record-structs.md](record-structs.md) |
| Melhorias em tipos estrutura (structs, `with`, …) | [structure-types-improvements.md](structure-types-improvements.md) |
| *Handlers* de strings interpoladas | [interpolated-string-handlers.md](interpolated-string-handlers.md) |
| Diretivas `global using` | [global-usings.md](global-usings.md) |
| `namespace` ao âmbito do ficheiro | [file-scoped-namespace.md](file-scoped-namespace.md) |
| *Property patterns* alargados | [extended-property-patterns.md](extended-property-patterns.md) |
| Tipo natural da lambda | [lambda-natural-type.md](lambda-natural-type.md) |
| Tipo de retorno explícito em lambda | [lambda-explicit-return-type.md](lambda-explicit-return-type.md) |
| Atributos em expressões lambda | [attributes-on-lambda-expressions.md](attributes-on-lambda-expressions.md) |
| `const string` com interpolação (placeholders constantes) | [const-string-interpolation.md](const-string-interpolation.md) |
| `sealed` em `ToString` sobre *record* | [record-tostring-sealed.md](record-tostring-sealed.md) |
| Análise de atribuição / estado nulo (avisos) | [null-analysis-improvements.md](null-analysis-improvements.md) |
| Desconstrução: declaração e atribuição juntas | [deconstruction-assignment-declaration.md](deconstruction-assignment-declaration.md) |
| `[AsyncMethodBuilder]` em métodos | [async-method-builder-attribute.md](async-method-builder-attribute.md) |
| `[CallerArgumentExpression]` | [caller-argument-expression.md](caller-argument-expression.md) |
| Formato novo do pragma `#line` | [line-pragma-csharp-10.md](line-pragma-csharp-10.md) |
| Funcionalidades *preview* (C# 10) | [preview-features-csharp-10.md](preview-features-csharp-10.md) |

## Edições anteriores na mesma pasta

Guias **9.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[record-structs.md](record-structs.md) ou [global-usings.md](global-usings.md)
