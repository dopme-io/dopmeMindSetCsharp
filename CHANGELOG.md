# Changelog

## [Unreleased]

### Adicionado

- Projeto **`MindSetCSharp10_0.Console`**: roteiro **C# 10.0** (novembro 2021, .NET 6) com **[csharp-10-0-overview.md](MindSetCSharp10_0.Console/Docs/csharp-10-0-overview.md)** e guias dedicados (*record structs*, melhorias em tipos estrutura, *handlers* de strings interpoladas, `global using`, `namespace` ao âmbito do ficheiro, *property patterns* alargados, lambdas com tipo natural / retorno explícito / atributos, `const string` com interpolação, `sealed` em `ToString` de *record*, análise nulo mais precisa, desconstrução mista, `[AsyncMethodBuilder]` em métodos, `[CallerArgumentExpression]`, pragma `#line` novo, notas sobre *preview*, …); inclui guias **9.0**/… em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp9_0.Console`**: roteiro **C# 9.0** (novembro 2020, .NET 5) com **[csharp-9-0-overview.md](MindSetCSharp9_0.Console/Docs/csharp-9-0-overview.md)** e guias dedicados (*records*, `init`, top-level statements, patterns relacionais e lógicos, `nint`/`nuint`, function pointers, `SkipLocalsInit`, module initializers, métodos parciais alargados, `new()` / `?:` com tipo alvo, funções anónimas `static`, retornos covariantes, `GetEnumerator` de extensão para `foreach`, descartes em lambdas, atributos em funções locais, …); inclui guias **8.0**/… em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp8_0.Console`**: roteiro **C# 8.0** (setembro 2019, .NET Core 3.0) com **[csharp-8-0-overview.md](MindSetCSharp8_0.Console/Docs/csharp-8-0-overview.md)** e guias dedicados (membros `readonly`, default interface members, expressões `switch`, *property*/*tuple*/*positional patterns*, `using` declarations, funções locais `static`, `ref struct` descartável, nullable reference types, `IAsyncEnumerable`, `Index`/`Range`, `??=`, tipos construídos `unmanaged`, `stackalloc` em expressões aninhadas, interpolação verbatim melhorada, …); inclui guias **7.3**/… em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp7_3.Console`**: roteiro **C# 7.3** (maio 2018) com **[csharp-7-3-overview.md](MindSetCSharp7_3.Console/Docs/csharp-7-3-overview.md)** e guias dedicados (`where T : unmanaged`, tuplos com `==`/`!=`, variáveis de expressão, `[field: …]` em propriedades autoimplementadas, resolução de overload, `-publicsign` / `-pathmap`, tema desempenho/código seguro com ligação a 7.2, …); inclui guias **7.2**/… em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp7_2.Console`**: roteiro **C# 7.2** (novembro 2017) com **[csharp-7-2-overview.md](MindSetCSharp7_2.Console/Docs/csharp-7-2-overview.md)** e guias dedicados (`readonly struct`, `ref struct`, `in`, `ref readonly`, `stackalloc` com inicializadores, `fixed`, `private protected`, argumentos nomeados não finais, expressão condicional `ref`, nota sobre restrições genéricas vs 7.3, …); inclui guias **7.1**/**7.0**/… em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp7_1.Console`**: roteiro **C# 7.1** (agosto 2017; primeiro lançamento pontual) com **[csharp-7-1-overview.md](MindSetCSharp7_1.Console/Docs/csharp-7-1-overview.md)** e guias dedicados (`async Main`, literal `default` inferido, nomes de tuplo inferidos, pattern matching com parâmetro de tipo genérico, `LangVersion`, `-refout` / `-refonly`); inclui guias **7.0** e anteriores em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp7_0.Console`**: roteiro **C# 7.0** (março 2017, Visual Studio 2017) com **[csharp-7-0-overview.md](MindSetCSharp7_0.Console/Docs/csharp-7-0-overview.md)** e guias dedicados (`out var`, tuplos, pattern matching, funções locais, `ref`, discards, literais binários, `throw` expression, …); guias até **5.0** em cópia local; **sem** projeto MindSet **6.0**; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp5_0.Console`**: roteiro **C# 5.0** (agosto 2012, Visual Studio 2012, .NET Framework 4.5) com **[csharp-5-0-overview.md](MindSetCSharp5_0.Console/Docs/csharp-5-0-overview.md)** e guias dedicados (`async`/`await`, atributos de informação do chamador); guias anteriores em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp4_0.Console`**: roteiro **C# 4.0** (abril 2010, Visual Studio 2010, .NET Framework 4) com **[csharp-4-0-overview.md](MindSetCSharp4_0.Console/Docs/csharp-4-0-overview.md)** e guias dedicados (`dynamic`, argumentos nomeados/opcionais, variança `out`/`in` em interfaces, tipos de interop incorporados); inclui guias 3.0/2.0 e base 1.0 em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp3_0.Console`**: roteiro **C# 3.0** (final de 2007, Visual Studio 2008; funcionalidades completas com **.NET Framework 3.5**) com **[csharp-3-0-overview.md](MindSetCSharp3_0.Console/Docs/csharp-3-0-overview.md)** e guias dedicados (LINQ, lambdas, extension methods, `var`, expression trees, tipos anónimos, inicializadores, auto-properties, métodos parciais); inclui guias 2.0 e base 1.0 em cópia local; projeto em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp2_0.Console`**: roteiro **C# 2.0** (novembro 2005, Visual Studio 2005, .NET 2.0) com **[csharp-2-0-overview.md](MindSetCSharp2_0.Console/Docs/csharp-2-0-overview.md)** e guias dedicados (genéricos, tipos parciais, métodos anónimos, nullable, iteradores, covariância/contravariância enquadrada, outras melhorias); base 1.0 em cópia local; projeto incluído em **`MindSetCSharp.sln`**.
- Projeto **`MindSetCSharp1_2.Console`**: mesma estrutura que a edição 1.0 (`Program.cs` + `Docs/`), roteiro **C# 1.2** (abril 2003, Visual Studio .NET 2003), com **[csharp-1-2-enhancements.md](MindSetCSharp1_2.Console/Docs/csharp-1-2-enhancements.md)** sobre **`foreach`** e **`Dispose()`** em **`IEnumerator`** que implementa **`IDisposable`**; restantes guias copiados da base 1.0 com referências atualizadas.
- Roteiro **C# 1.0** em `MindSetCSharp1_0.Console/Docs/`: nove guias (classes, structs, interfaces, eventos, propriedades, delegates, operadores/expressões, statements, atributos) + `Docs/README.md`, alinhados ao lançamento de janeiro de 2002 / Visual Studio .NET 2002.

### Alterado

- Removidas do console as pastas de módulos temáticos e a infraestrutura interna (`Pipeline/`, `Factories/`, etc.); o `Program.cs` apenas orienta para `Docs/`.
- Documentação na raiz e índices atualizados para o modelo **documentação + exemplos copiáveis**.

### Histórico anterior

- Solução só com console `MindSetCSharp1_0.Console`; sem `Core` / `Application` / `Tests`.
- CI sem `dotnet test` enquanto não existir projeto de testes.
- Remoção de `ARCHITECTURE.md` / `ARCHITECTURE_DIAGRAM.md` em favor do formato documentado na raiz.

## [1.0.0] - YYYY-MM-DD

### Adicionado

- Inicialização do repositório.
