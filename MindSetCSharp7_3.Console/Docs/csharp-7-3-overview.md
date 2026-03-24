# C# 7.3 — visão geral (maio 2018)

## Contexto

**C# 7.3** consolidou dois **eixos**: (1) **código seguro** com desempenho próximo do **unsafe** — continuando trabalho iniciado em **7.2** (`ref`, `stackalloc`, `fixed`, …) e acrescentando sobretudo a restrição **`unmanaged`**; (2) **melhorias incrementais** em funcionalidades já existentes (tuplos, variáveis de expressão, propriedades automáticas, resolução de overload com **`in`**).

Saíram também novas **opções de compilador** orientadas a **OSS** e a **caminhos de fonte** reprodutíveis em CI.

## Funcionalidades C# 7.3 (guias dedicados)

| Tema | Ficheiro |
|------|----------|
| Restrição `where T : unmanaged` | [generic-constraint-unmanaged.md](generic-constraint-unmanaged.md) |
| Tema desempenho / código seguro (ligação a 7.2) | [safe-code-performance-theme-7-3.md](safe-code-performance-theme-7-3.md) |
| `==` e `!=` em tipos tuplo | [tuple-equality-operators.md](tuple-equality-operators.md) |
| Variáveis de expressão em mais contextos | [expression-variables-extended.md](expression-variables-extended.md) |
| Atributos no *backing field* de propriedades autoimplementadas | [attribute-backing-field-auto-properties.md](attribute-backing-field-auto-properties.md) |
| Resolução de métodos / overloads (`in`, menos ambiguidade) | [overload-resolution-improvements-7-3.md](overload-resolution-improvements-7-3.md) |
| Compilador: `-publicsign`, `-pathmap` | [compiler-publicsign-pathmap.md](compiler-publicsign-pathmap.md) |

## Edições anteriores na mesma pasta

Guias **7.2**, **7.1**, **7.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[generic-constraint-unmanaged.md](generic-constraint-unmanaged.md) ou [tuple-equality-operators.md](tuple-equality-operators.md)

**Continuar para C# 8.0** (setembro 2019, .NET Core 3.0): [MindSetCSharp8_0.Console/Docs/README.md](../../MindSetCSharp8_0.Console/Docs/README.md) — comece por [csharp-8-0-overview.md](../../MindSetCSharp8_0.Console/Docs/csharp-8-0-overview.md).

**Continuar para C# 9.0** (novembro 2020, .NET 5): [MindSetCSharp9_0.Console/Docs/README.md](../../MindSetCSharp9_0.Console/Docs/README.md) — comece por [csharp-9-0-overview.md](../../MindSetCSharp9_0.Console/Docs/csharp-9-0-overview.md).

**Continuar para C# 10.0** (novembro 2021, .NET 6): [MindSetCSharp10_0.Console/Docs/README.md](../../MindSetCSharp10_0.Console/Docs/README.md) — comece por [csharp-10-0-overview.md](../../MindSetCSharp10_0.Console/Docs/csharp-10-0-overview.md).
