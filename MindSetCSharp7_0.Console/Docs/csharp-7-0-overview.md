# C# 7.0 — visão geral (março 2017)

## Contexto

**C# 7.0** saiu com o **Visual Studio 2017**, na mesma época em que **.NET Core** ganhava tração **multiplataforma** e foco em **cloud** e **portabilidade**. A linguagem continuou na linha da **6.0**: muitas melhorias **incrementais** que **eliminam boilerplate** e abrem formas **mais expressivas** de escrever código.

Destaques práticos: declarar variáveis **`out`** no sítio da chamada (`TryParse` sem linha extra antes), **tuplos** com **múltiplos valores de retorno** e **desconstrução**, **pattern matching** inicial (`is`, `switch`), **funções locais**, **`ref` locals e retornos**, **`_` discards**, **literais binários** e **separadores de dígitos**, e **`throw`** como expressão.

## Mindset

- **Tuplos + `out`**: menos tipos “só para transportar dois números” e menos variáveis temporárias óbvias.
- **Pattern matching**: começar a pensar em **forma** dos dados, não só em tipos estáticos — a funcionalidade cresce nas versões seguintes.
- **.NET Core / portabilidade**: o ecossistema puxava por APIs e estilos que funcionem bem em **Linux**, **contentores** e serviços.

## Nota sobre C# 6.0

Neste repositório **não há** (ainda) um projeto `MindSetCSharp6_0.Console`; a **6.0** (interpolação de strings, `nameof`, `?.`, `using static`, …) costuma estar coberta por materiais externos ou por uma futura edição MindSet. Os exemplos **7.0** assumem **SDK atual** e compilador recente.

## Próximo passo

[out-variables.md](out-variables.md) ou [tuples-deconstruction.md](tuples-deconstruction.md)

**Continuar para C# 7.1** (agosto 2017): no projeto [MindSetCSharp7_1.Console](../../MindSetCSharp7_1.Console/Docs/README.md), comece por [csharp-7-1-overview.md](../../MindSetCSharp7_1.Console/Docs/csharp-7-1-overview.md).
