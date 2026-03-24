# Formato do projeto MindSet C#

A solução contém **apenas projetos console** (um por edição da linguagem / MindSet).

## Edições na solução

### MindSet C# 1.0 — `MindSetCSharp1_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Roteiro **C# 1.0 (2002)** — um ficheiro por recurso (classes, structs, …) |

### MindSet C# 1.2 — `MindSetCSharp1_2.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Mesma estrutura de tópicos base 1.0 + **[csharp-1-2-enhancements.md](MindSetCSharp1_2.Console/Docs/csharp-1-2-enhancements.md)** (foreach, `IEnumerator`, `Dispose`, VS .NET **2003**) |

### MindSet C# 2.0 — `MindSetCSharp2_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Base 1.0 em cópia local + guias **2.0** (genéricos, tipos parciais, métodos anónimos, nullable, iteradores, covariância/contravariância enquadrada, outras melhorias) — ver [csharp-2-0-overview.md](MindSetCSharp2_0.Console/Docs/csharp-2-0-overview.md); **.NET 2.0 / VS 2005** |

### MindSet C# 3.0 — `MindSetCSharp3_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Base 1.0 + guias **2.0** em cópia local + guias **3.0** (LINQ, lambdas, `var`, extension methods, expression trees, tipos anónimos, inicializadores, auto-properties, métodos parciais) — [csharp-3-0-overview.md](MindSetCSharp3_0.Console/Docs/csharp-3-0-overview.md); **.NET 3.5 / VS 2008** |

### MindSet C# 4.0 — `MindSetCSharp4_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Guias **3.0**, **2.0** e base **1.0** em cópia local + guias **4.0** (`dynamic`, argumentos nomeados/opcionais, variança `out`/`in` em interfaces, interop incorporado) — [csharp-4-0-overview.md](MindSetCSharp4_0.Console/Docs/csharp-4-0-overview.md); **.NET 4 / VS 2010** |

### MindSet C# 5.0 — `MindSetCSharp5_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Guias **4.0** … **1.0** em cópia local + guias **5.0** (`async`/`await`, atributos *caller info*) — [csharp-5-0-overview.md](MindSetCSharp5_0.Console/Docs/csharp-5-0-overview.md); **.NET 4.5 / VS 2012** |

### MindSet C# 7.0 — `MindSetCSharp7_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Guias **5.0** … **1.0** em cópia local + guias **7.0** (`out var`, tuplos, pattern matching, funções locais, `ref`, discards, literais binários, `throw` expr.) — [csharp-7-0-overview.md](MindSetCSharp7_0.Console/Docs/csharp-7-0-overview.md); **VS 2017** / **.NET Core** em expansão. *Não há projeto MindSet C# 6.0 no repositório.* |

### MindSet C# 7.1 — `MindSetCSharp7_1.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **7.0** e anteriores + guias **7.1** (`async Main`, literal `default` inferido, nomes de tuplo inferidos, pattern matching com `T` genérico, `LangVersion`, `-refout` / `-refonly`) — [csharp-7-1-overview.md](MindSetCSharp7_1.Console/Docs/csharp-7-1-overview.md); **agosto 2017**, primeiro lançamento pontual |

### MindSet C# 7.2 — `MindSetCSharp7_2.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **7.1**/**7.0**/… + guias **7.2** (`readonly struct`, `ref struct`, `in`, `ref readonly`, `stackalloc` com inicializadores, `fixed` alargado, `private protected`, argumentos nomeados não finais, expressão condicional `ref`, …) — [csharp-7-2-overview.md](MindSetCSharp7_2.Console/Docs/csharp-7-2-overview.md); **novembro 2017** |

### MindSet C# 7.3 — `MindSetCSharp7_3.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **7.2**/… + guias **7.3** (`where T : unmanaged`, `==`/`!=` em tuplos, variáveis de expressão, `[field: …]`, resolução de overload, `-publicsign`, `-pathmap`, …) — [csharp-7-3-overview.md](MindSetCSharp7_3.Console/Docs/csharp-7-3-overview.md); **maio 2018** |

### MindSet C# 8.0 — `MindSetCSharp8_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **7.3**/… + guias **8.0** (membros `readonly`, default interface members, patterns, `using` declarations, funções locais `static`, NRT, `IAsyncEnumerable`, `Index`/`Range`, `??=`, …) — [csharp-8-0-overview.md](MindSetCSharp8_0.Console/Docs/csharp-8-0-overview.md); **setembro 2019** / **.NET Core 3.0** |

### MindSet C# 9.0 — `MindSetCSharp9_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **8.0**/… + guias **9.0** (*records*, `init`, top-level statements, patterns relacionais/lógicos, `nint`/`nuint`, function pointers, module initializers, …) — [csharp-9-0-overview.md](MindSetCSharp9_0.Console/Docs/csharp-9-0-overview.md); **novembro 2020** / **.NET 5** |

### MindSet C# 10.0 — `MindSetCSharp10_0.Console`

| Conteúdo | Descrição |
|----------|-----------|
| `Program.cs` | Entrada; aponta para `Docs/` |
| `Docs/` | Cópia dos guias **9.0**/… + guias **10.0** (*record structs*, `global using`, *handlers* de interpolação, `namespace` por ficheiro, lambdas, …) — [csharp-10-0-overview.md](MindSetCSharp10_0.Console/Docs/csharp-10-0-overview.md); **novembro 2021** / **.NET 6** |

## Nome no disco

| Nome pedagógico | Projeto |
|-----------------|---------|
| MindSet C# 1.0 | `MindSetCSharp1_0.Console` |
| MindSet C# 1.2 | `MindSetCSharp1_2.Console` |
| MindSet C# 2.0 | `MindSetCSharp2_0.Console` |
| MindSet C# 3.0 | `MindSetCSharp3_0.Console` |
| MindSet C# 4.0 | `MindSetCSharp4_0.Console` |
| MindSet C# 5.0 | `MindSetCSharp5_0.Console` |
| MindSet C# 7.0 | `MindSetCSharp7_0.Console` |
| MindSet C# 7.1 | `MindSetCSharp7_1.Console` |
| MindSet C# 7.2 | `MindSetCSharp7_2.Console` |
| MindSet C# 7.3 | `MindSetCSharp7_3.Console` |
| MindSet C# 8.0 | `MindSetCSharp8_0.Console` |
| MindSet C# 9.0 | `MindSetCSharp9_0.Console` |
| MindSet C# 10.0 | `MindSetCSharp10_0.Console` |

## Nova edição

Crie outro projeto console (ex.: `MindSetCSharp11_0.Console`), adicione à solução, crie `Docs/` no mesmo padrão e atualize este ficheiro e o [README.md](README.md).

## Ligações

- C# 1.0: [MindSetCSharp1_0.Console/Docs/README.md](MindSetCSharp1_0.Console/Docs/README.md)
- C# 1.2: [MindSetCSharp1_2.Console/Docs/README.md](MindSetCSharp1_2.Console/Docs/README.md)
- C# 2.0: [MindSetCSharp2_0.Console/Docs/README.md](MindSetCSharp2_0.Console/Docs/README.md)
- C# 3.0: [MindSetCSharp3_0.Console/Docs/README.md](MindSetCSharp3_0.Console/Docs/README.md)
- C# 4.0: [MindSetCSharp4_0.Console/Docs/README.md](MindSetCSharp4_0.Console/Docs/README.md)
- C# 5.0: [MindSetCSharp5_0.Console/Docs/README.md](MindSetCSharp5_0.Console/Docs/README.md)
- C# 7.0: [MindSetCSharp7_0.Console/Docs/README.md](MindSetCSharp7_0.Console/Docs/README.md)
- C# 7.1: [MindSetCSharp7_1.Console/Docs/README.md](MindSetCSharp7_1.Console/Docs/README.md)
- C# 7.2: [MindSetCSharp7_2.Console/Docs/README.md](MindSetCSharp7_2.Console/Docs/README.md)
- C# 7.3: [MindSetCSharp7_3.Console/Docs/README.md](MindSetCSharp7_3.Console/Docs/README.md)
- C# 8.0: [MindSetCSharp8_0.Console/Docs/README.md](MindSetCSharp8_0.Console/Docs/README.md)
- C# 9.0: [MindSetCSharp9_0.Console/Docs/README.md](MindSetCSharp9_0.Console/Docs/README.md)
- C# 10.0: [MindSetCSharp10_0.Console/Docs/README.md](MindSetCSharp10_0.Console/Docs/README.md)
- Índice geral: [DOCUMENTATION_INDEX.md](DOCUMENTATION_INDEX.md)
