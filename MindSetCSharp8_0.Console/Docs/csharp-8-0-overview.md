# C# 8.0 — visão geral (setembro 2019)

## Contexto

**C# 8.0** foi a primeira **grande** versão da linguagem orientada de forma explícita para **.NET Core**. Parte das funcionalidades depende de **novidades na CLR** (Common Language Runtime) ou de **tipos de biblioteca** introduzidos com **.NET Core 3.0** — por exemplo, **membros predefinidos de interface** exigem alterações na CLR; **índices**, **intervalos** e **fluxos assíncronos** dependem de tipos (`Index`, `Range`, `IAsyncEnumerable<T>`, …) nas bibliotecas.

**Tipos de referência anuláveis** (*nullable reference types*) são sobretudo úteis quando as **bibliotecas base** vão sendo **anotadas** (contratos sobre `null` em argumentos e valores de retorno).

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| Membros `readonly` em structs | [readonly-members.md](readonly-members.md) |
| Membros predefinidos de interface | [default-interface-members.md](default-interface-members.md) |
| Expressões `switch` | [pattern-switch-expressions.md](pattern-switch-expressions.md) |
| *Property patterns* | [pattern-property-patterns.md](pattern-property-patterns.md) |
| *Tuple patterns* | [pattern-tuple-patterns.md](pattern-tuple-patterns.md) |
| *Positional patterns* | [pattern-positional-patterns.md](pattern-positional-patterns.md) |
| Declarações `using` | [using-declarations.md](using-declarations.md) |
| Funções locais `static` | [static-local-functions.md](static-local-functions.md) |
| `ref struct` descartável (`IDisposable`) | [disposable-ref-structs.md](disposable-ref-structs.md) |
| Tipos de referência anuláveis | [nullable-reference-types.md](nullable-reference-types.md) |
| Fluxos assíncronos (`IAsyncEnumerable`) | [asynchronous-streams.md](asynchronous-streams.md) |
| Índices e intervalos | [indices-and-ranges.md](indices-and-ranges.md) |
| Atribuição de coalescência nula (`??=`) | [null-coalescing-assignment.md](null-coalescing-assignment.md) |
| Tipos construídos geridos `unmanaged` | [unmanaged-constructed-types.md](unmanaged-constructed-types.md) |
| `stackalloc` em expressões aninhadas | [stackalloc-nested-expressions.md](stackalloc-nested-expressions.md) |
| Interpolação + *verbatim* melhorada | [interpolated-verbatim-strings-8-0.md](interpolated-verbatim-strings-8-0.md) |

## Edições anteriores na mesma pasta

Guias **7.3** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[nullable-reference-types.md](nullable-reference-types.md) ou [indices-and-ranges.md](indices-and-ranges.md)

## Continuar para C# 9.0 (novembro 2020, .NET 5)

[MindSetCSharp9_0.Console/Docs/README.md](../../MindSetCSharp9_0.Console/Docs/README.md) — comece por [csharp-9-0-overview.md](../../MindSetCSharp9_0.Console/Docs/csharp-9-0-overview.md).

**Continuar para C# 10.0** (novembro 2021, .NET 6): [MindSetCSharp10_0.Console/Docs/README.md](../../MindSetCSharp10_0.Console/Docs/README.md) — comece por [csharp-10-0-overview.md](../../MindSetCSharp10_0.Console/Docs/csharp-10-0-overview.md).
