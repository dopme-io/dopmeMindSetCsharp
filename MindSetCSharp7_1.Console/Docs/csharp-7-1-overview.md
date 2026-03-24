# C# 7.1 — visão geral (agosto 2017)

## Contexto

**C# 7.1** foi o primeiro **lançamento pontual** da linguagem após **7.0**: a equipa passou a entregar **7.1**, **7.2**, **7.3** com ciclos mais curtos, em paralelo com o **Visual Studio 2017** (atualizações) e o ecossistema **.NET Core**.

Nesta versão surgiram três melhorias de linguagem bem visíveis no dia a dia, mais **pattern matching** alargado a **parâmetros de tipo genérico**, e infraestrutura importante:

- **Seleção da versão da linguagem** no projeto (`LangVersion` no `.csproj` ou equivalente), para fixar **7.0**, **7.1**, **latest**, etc., em vez de ficar preso à versão predefinida do compilador.
- Opções de compilador **`-refout`** e **`-refonly`**, que controlam a geração de **reference assemblies** (assemblies só com metadados públicos, úteis em builds em camadas e ferramentas).

## Funcionalidades de linguagem (7.1)

| Tópico | Ficheiro |
|--------|----------|
| `async` no `Main` | [async-main-method.md](async-main-method.md) |
| Literal `default` com tipo inferido | [default-literal.md](default-literal.md) |
| Nomes de elementos de tuplo inferidos | [inferred-tuple-element-names.md](inferred-tuple-element-names.md) |
| Pattern matching em `T` genérico | [pattern-matching-generic-type-parameters.md](pattern-matching-generic-type-parameters.md) |

## Compilador e projeto

| Tópico | Ficheiro |
|--------|----------|
| `LangVersion`, `-refout`, `-refonly` | [langversion-ref-assemblies.md](langversion-ref-assemblies.md) |

## Relação com C# 7.0

Os guias **7.0** (`out var`, tuplos, patterns iniciais, …) estão na **mesma pasta** (cópia do roteiro MindSet). Comece por [csharp-7-0-overview.md](csharp-7-0-overview.md) se quiser ordem estrita **7.0 → 7.1**.

## Próximo passo

[async-main-method.md](async-main-method.md) ou [langversion-ref-assemblies.md](langversion-ref-assemblies.md)

**Continuar para C# 7.2** (novembro 2017): [MindSetCSharp7_2.Console/Docs/README.md](../../MindSetCSharp7_2.Console/Docs/README.md) — comece por [csharp-7-2-overview.md](../../MindSetCSharp7_2.Console/Docs/csharp-7-2-overview.md).

**Continuar para C# 7.3** (maio 2018): [MindSetCSharp7_3.Console/Docs/README.md](../../MindSetCSharp7_3.Console/Docs/README.md) — comece por [csharp-7-3-overview.md](../../MindSetCSharp7_3.Console/Docs/csharp-7-3-overview.md).
