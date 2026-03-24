# Resumo do estado — MindSetCSharp

## Edições

| Edição | Projeto | Destaque em `Docs/` |
|--------|---------|---------------------|
| MindSet C# 1.0 | `MindSetCSharp1_0.Console` | Nove tópicos base (2002) |
| MindSet C# 1.2 | `MindSetCSharp1_2.Console` | Mesma base + **csharp-1-2-enhancements.md** (foreach / `Dispose` no `IEnumerator`, 2003) |
| MindSet C# 2.0 | `MindSetCSharp2_0.Console` | Base 1.0 + guias 2.0 (**csharp-2-0-overview.md**, genéricos, iteradores, nullable, …, 2005) |
| MindSet C# 3.0 | `MindSetCSharp3_0.Console` | Guias 2.0 + base 1.0 + guias 3.0 (**csharp-3-0-overview.md**, LINQ, lambdas, …, 2007–2008) |
| MindSet C# 4.0 | `MindSetCSharp4_0.Console` | Guias 3.0/2.0 + base 1.0 + guias 4.0 (**csharp-4-0-overview.md**, `dynamic`, NoPIA, …, 2010) |
| MindSet C# 5.0 | `MindSetCSharp5_0.Console` | Guias anteriores em cópia + guias 5.0 (**csharp-5-0-overview.md**, `async`/`await`, caller info, …, 2012) |
| MindSet C# 7.0 | `MindSetCSharp7_0.Console` | Guias até 5.0 em cópia + guias 7.0 (**csharp-7-0-overview.md**, tuplos, `out var`, …, 2017; sem MindSet 6.0) |
| MindSet C# 7.1 | `MindSetCSharp7_1.Console` | Guias 7.0 e anteriores em cópia + guias 7.1 (**csharp-7-1-overview.md**, `async Main`, `default`, tuplos, patterns em `T`, `LangVersion`, `-refout` / `-refonly`, 2017) |
| MindSet C# 7.2 | `MindSetCSharp7_2.Console` | Guias 7.1/7.0 em cópia + guias 7.2 (**csharp-7-2-overview.md**, `readonly`/`ref struct`, `in`, `stackalloc`, `fixed`, `private protected`, …, 2017) |
| MindSet C# 7.3 | `MindSetCSharp7_3.Console` | Guias 7.2 em cópia + guias 7.3 (**csharp-7-3-overview.md**, `unmanaged`, tuplos `==`, `[field: …]`, `-publicsign` / `-pathmap`, …, 2018) |
| MindSet C# 8.0 | `MindSetCSharp8_0.Console` | Guias 7.3 em cópia + guias 8.0 (**csharp-8-0-overview.md**, NRT, default interface members, `switch` expressions, `IAsyncEnumerable`, índices/ranges, …, 2019) |
| MindSet C# 9.0 | `MindSetCSharp9_0.Console` | Guias 8.0 em cópia + guias 9.0 (**csharp-9-0-overview.md**, records, top-level statements, patterns relacionais, .NET 5, …, 2020) |
| MindSet C# 10.0 | `MindSetCSharp10_0.Console` | Guias 9.0 em cópia + guias 10.0 (**csharp-10-0-overview.md**, *record structs*, `global using`, .NET 6, …, 2021) |

## Documentação raiz

[README.md](README.md), [DOCUMENTATION.md](DOCUMENTATION.md), [DOCUMENTATION_INDEX.md](DOCUMENTATION_INDEX.md), [FORMATO_DO_PROJETO.md](FORMATO_DO_PROJETO.md).

## CI / releases

Os workflows publicam **todos** os `.csproj` com `<OutputType>Exe</OutputType>` (inclui todas as edições na solução).
