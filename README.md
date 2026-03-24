<div align="center">
  <img width="263" height="182" alt="dopme io" src="https://github.com/dopme-io/dopmeRepo/blob/main/assests/Use%20Mindset%20com%20CSharp.png" />
  </br>
  <img width="663" height="69" src="https://github.com/dopme-io/dopmeRepo/blob/main/assests/MindSet%20CSharp.png" />

  [![.NET](https://github.com/dopme-io/UseMindCSharp/actions/workflows/dotnet.yml/badge.svg)](https://github.com/dopme-io/UseMindCSharp/actions/workflows/dotnet.yml)
  ![Versão](https://img.shields.io/badge/.NET-10.0-blue)
  
  Repositório educacional focado em fundamentos de programação C# com abordagem Mindset. Explora conceitos essenciais através de uma mentalidade eficaz para o desenvolvimento de software em C#.
</div>


---

## Índice

- [Sobre](#sobre)
- [Tecnologias](#tecnologias)
- [Formato do projeto](#formato-do-projeto)
- [Instalação](#instalação)
- [Uso](#uso)
- [Roteiros por edição](#roteiros-por-edição)
- [Contribuição](#contribuição)
- [Licença](#licença)
- [Contato](#contato)

---

## Sobre

Este projeto faz parte do ecossistema `dopme-io` e tem como objetivo principal explorar a base fundamental da programação em C# através da abordagem Mindset.

### O que você aprenderá

- **C# 1.0** (2002): pilares da linguagem (classes, structs, interfaces, eventos, propriedades, delegates, operadores/expressões, instruções, atributos).
- **C# 1.2** (2003, Visual Studio .NET 2003): melhorias pontuais, em destaque o **`foreach`** que passa a chamar **`Dispose()`** em **`IEnumerator`** quando implementa **`IDisposable`**.
- **C# 2.0** (2005, Visual Studio 2005, .NET 2.0): **genéricos**, **tipos parciais**, **métodos anónimos**, **nullable** para tipos valor, **iteradores** (`yield`), enquadramento de **covariância/contravariância**, e refinamentos (acessibilidade get/set, classes estáticas, grupo de métodos, inferência de delegado).
- **C# 3.0** (2007, Visual Studio 2008, .NET 3.5): **LINQ** (expressões de consulta + `System.Linq`), **lambdas**, **métodos de extensão**, **`var`**, **inicializadores**, **tipos anónimos**, **árvores de expressão**, **propriedades autoimplementadas**, **métodos parciais** — base híbrida OO / declarativa (ex.: `list.Average()` em coleções).
- **C# 4.0** (2010, Visual Studio 2010, .NET 4): **`dynamic`** (ligação adiada / DLR), **argumentos nomeados** e **parâmetros opcionais**, **covariância/contravariância** em interfaces genéricas (`out` / `in`), **tipos de interop COM incorporados** (NoPIA).
- **C# 5.0** (2012, Visual Studio 2012, .NET 4.5): **`async`** / **`await`** como modelo de assincronia de **primeira classe**; **atributos de informação do chamador** (`CallerMemberName`, `CallerFilePath`, `CallerLineNumber`) para diagnóstico e logging sem reflexão repetitiva.
- **C# 7.0** (2017, Visual Studio 2017): **`out var`**, **tuplos** e **desconstrução**, **pattern matching** inicial, **funções locais**, **`ref` locals/returns**, **discards**, **literais binários** / **separadores de dígitos**, **`throw`** como expressão — no espírito da 6.0 (menos boilerplate); contexto **.NET Core** multiplataforma. *(Não há projeto MindSet C# 6.0 neste repositório.)*
- **C# 7.1** (agosto 2017): primeiro **lançamento pontual**; **`async Main`**, literal **`default`** com tipo inferido, **nomes de elementos de tuplo inferidos**, **pattern matching** com operandos de tipo **genérico `T`**, **`LangVersion`** no projeto, compilador **`-refout`** / **`-refonly`** (reference assemblies).
- **C# 7.2** (novembro 2017): **`readonly struct`**, **`ref struct`**, **`in`**, **`ref readonly`**, reatribuição de **`ref` locals**, **`stackalloc`** com inicializadores, **`fixed`** alargado, **`private protected`**, argumentos nomeados **não finais**, **`_`** em literais numéricos, expressão condicional **`ref`**, e nota sobre restrições genéricas vs **7.3**.
- **C# 7.3** (maio 2018): **`where T : unmanaged`**; **`==`/`!=`** em tuplos; variáveis de expressão em mais sítios; **`[field: …]`** em propriedades autoimplementadas; melhorias na resolução de overload (incl. **`in`**); compilador **`-publicsign`** (OSS signing) e **`-pathmap`** (mapeamento de caminhos de fonte); continuação do tema **código seguro** com desempenho (complementa **7.2**).
- **C# 8.0** (setembro 2019): primeira grande versão focada em **.NET Core 3.0** — membros **`readonly`** e **predefinidos de interface** (CLR), **patterns** (expressões `switch`, propriedade, tuplo, posicional), **`using` declarations**, funções locais **`static`**, **`ref struct`** descartável, **tipos de referência anuláveis**, **`IAsyncEnumerable`**, **`Index`/`Range`**, **`??=`**, tipos construídos **`unmanaged`**, **`stackalloc`** em expressões aninhadas, interpolação verbatim melhorada.
- **C# 9.0** (novembro 2020): com **.NET 5** (versão predefinida da linguagem para esse alvo) — **records**, **`init`**, **instruções de nível superior**, **patterns** relacionais e lógicos (`<`, `>`, `and`, `or`, `not`, `is not null`), **`nint`/`nuint`**, **ponteiros de função**, **inicializadores de módulo**, **métodos parciais** alargados, **`new()`** e **`?:`** com tipo alvo, **retornos covariantes**, **`GetEnumerator`** de extensão para **`foreach`**, lambdas **`static`** e descartes, atributos em funções locais, …
- **C# 10.0** (novembro 2021): com **.NET 6** — **record structs**, melhorias em **structs** / tipos anónimos com **`with`**, **`global using`**, **`namespace` ao âmbito do ficheiro**, **handlers** de strings interpoladas, *property patterns* alargados, **lambdas** com tipo natural / retorno explícito / atributos, **`const string`** com interpolação, **`sealed`** em `ToString` de *record*, **`[CallerArgumentExpression]`**, **`[AsyncMethodBuilder]`** em métodos, pragma **`#line`** novo, *preview* (atributos genéricos, membros estáticos abstratos em interfaces), …
- Como praticar no **SDK .NET atual** a partir dos guias em **`Docs/`** de cada edição.
- Base para o que veio a seguir (C# 10+, …).

---

## Tecnologias

- [C# 12](https://learn.microsoft.com/dotnet/csharp/) nos projetos console (compilador atual; conteúdo dos `Docs/` é histórico 1.0 / 1.2 / 2.0 / 3.0 / 4.0 / 5.0 / 7.0 / 7.1 / 7.2 / 7.3 / 8.0 / 9.0 / 10.0)
- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)
- [Visual Studio](https://visualstudio.microsoft.com/pt-br/) ou [VS Code](https://code.visualstudio.com/)

---

## Formato do projeto

A solução contém **apenas projetos console** — sem bibliotecas separadas e sem projeto de testes.

| Edição (nome em documentação) | Projeto |
|------------------------------|---------|
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
| MindSet C# 11.0 | `MindSetCSharp11_0.Console` |
| MindSet C# 12.0 | `MindSetCSharp12_0.Console` |
| MindSet C# 13.0 | `MindSetCSharp13_0.Console` |
| MindSet C# 14.0 | `MindSetCSharp14_0.Console` |
| MindSet C# 15.0 | `MindSetCSharp15_0.Console` |

Cada projeto tem **`Docs/`**: em **1.0**, roteiro só da base inicial; em **1.2**, o mesmo conjunto de tópicos (cópia local) mais **[csharp-1-2-enhancements.md](MindSetCSharp1_2.Console/Docs/csharp-1-2-enhancements.md)** sobre **foreach** e **`Dispose`** no enumerador; em **2.0**, base 1.0 em cópia local mais guias dedicados (comece por **[csharp-2-0-overview.md](MindSetCSharp2_0.Console/Docs/csharp-2-0-overview.md)**); em **3.0**, cópia com guias 2.0 + base 1.0 mais guias **3.0** (comece por **[csharp-3-0-overview.md](MindSetCSharp3_0.Console/Docs/csharp-3-0-overview.md)**); em **4.0**, cópia com guias anteriores mais guias **4.0** (comece por **[csharp-4-0-overview.md](MindSetCSharp4_0.Console/Docs/csharp-4-0-overview.md)**); em **5.0**, cópia com guias anteriores mais guias **5.0** (comece por **[csharp-5-0-overview.md](MindSetCSharp5_0.Console/Docs/csharp-5-0-overview.md)**); em **7.0**, cópia com guias até **5.0** mais guias **7.0** (comece por **[csharp-7-0-overview.md](MindSetCSharp7_0.Console/Docs/csharp-7-0-overview.md)**) — **sem** projeto MindSet **6.0**; em **7.1**, a mesma cópia de fundação mais guias **7.1** (comece por **[csharp-7-1-overview.md](MindSetCSharp7_1.Console/Docs/csharp-7-1-overview.md)**); em **7.2**, cópia com guias **7.1**/**7.0**/… mais guias **7.2** (comece por **[csharp-7-2-overview.md](MindSetCSharp7_2.Console/Docs/csharp-7-2-overview.md)**); em **7.3**, cópia com guias **7.2**/… mais guias **7.3** (comece por **[csharp-7-3-overview.md](MindSetCSharp7_3.Console/Docs/csharp-7-3-overview.md)**); em **8.0**, cópia com guias **7.x**/… mais guias **8.0** (comece por **[csharp-8-0-overview.md](MindSetCSharp8_0.Console/Docs/csharp-8-0-overview.md)**) — **.NET Core 3.0**; em **9.0**, cópia com guias **8.0**/… mais guias **9.0** (comece por **[csharp-9-0-overview.md](MindSetCSharp9_0.Console/Docs/csharp-9-0-overview.md)**) — **.NET 5**; em **10.0**, cópia com guias **9.0**/… mais guias **10.0** (comece por **[csharp-10-0-overview.md](MindSetCSharp10_0.Console/Docs/csharp-10-0-overview.md)**) — **.NET 6**; em **11.0**, cópia com guias **10.0**/… mais guias **11.0** (comece por **[csharp-11-0-overview.md](MindSetCSharp11_0.Console/Docs/csharp-11-0-overview.md)**) — **.NET 7**, com **`LangVersion` 11** no `.csproj`; em **12.0**, cópia com guias **11.0**/… mais guias **12.0** (comece por **[csharp-12-0-overview.md](MindSetCSharp12_0.Console/Docs/csharp-12-0-overview.md)**) — **.NET 8**, com **`LangVersion` 12** no `.csproj`; em **13.0**, cópia com guias **12.0**/… mais guias **13.0** (comece por **[csharp-13-0-overview.md](MindSetCSharp13_0.Console/Docs/csharp-13-0-overview.md)**) — **.NET 9**, com **`LangVersion` 13** no `.csproj`; em **14.0**, cópia com guias **13.0**/… mais guias **14.0** (comece por **[csharp-14-0-overview.md](MindSetCSharp14_0.Console/Docs/csharp-14-0-overview.md)**) — **.NET 10**, com **`LangVersion` 14** no `.csproj`; em **15.0**, cópia com guias **14.0**/… mais guias **15.0** (comece por **[csharp-15-0-overview.md](MindSetCSharp15_0.Console/Docs/csharp-15-0-overview.md)**) — **.NET 11** (preview), com **`LangVersion` `preview`** ou **`15`** no `.csproj` conforme o SDK.

Leia os **README** de cada `Docs/`, **[FORMATO_DO_PROJETO.md](FORMATO_DO_PROJETO.md)** e **[DOCUMENTATION_INDEX.md](DOCUMENTATION_INDEX.md)**.

```
MindSetCSharp/
├── MindSetCSharp.sln
├── MindSetCSharp1_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp1_2.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp2_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp3_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp4_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp5_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp7_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp7_1.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp7_2.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp7_3.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp8_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp9_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp10_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp11_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp12_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp13_0.Console/
│   ├── Program.cs
│   └── Docs/
├── MindSetCSharp14_0.Console/
│   ├── Program.cs
│   └── Docs/
└── MindSetCSharp15_0.Console/
    ├── Program.cs
    └── Docs/
```

---

## Instalação

### Requisitos

- .NET 10 SDK ([download](https://dotnet.microsoft.com/download))

### Clonar e restaurar

```bash
git clone https://github.com/dopme-io/UseMindCSharp.git
cd UseMindCSharp
dotnet restore
```

---

## Uso

```bash
dotnet build
dotnet run --project MindSetCSharp1_0.Console
dotnet run --project MindSetCSharp1_2.Console
dotnet run --project MindSetCSharp2_0.Console
dotnet run --project MindSetCSharp3_0.Console
dotnet run --project MindSetCSharp4_0.Console
dotnet run --project MindSetCSharp5_0.Console
dotnet run --project MindSetCSharp7_0.Console
dotnet run --project MindSetCSharp7_1.Console
dotnet run --project MindSetCSharp7_2.Console
dotnet run --project MindSetCSharp7_3.Console
dotnet run --project MindSetCSharp8_0.Console
dotnet run --project MindSetCSharp9_0.Console
dotnet run --project MindSetCSharp10_0.Console
dotnet run --project MindSetCSharp11_0.Console
dotnet run --project MindSetCSharp12_0.Console
dotnet run --project MindSetCSharp13_0.Console
dotnet run --project MindSetCSharp14_0.Console
dotnet run --project MindSetCSharp15_0.Console
```

Release (`dotnet build -c Release`) segue o mesmo padrão.

---

## Roteiros por edição

- **C# 1.0:** [MindSetCSharp1_0.Console/Docs/README.md](MindSetCSharp1_0.Console/Docs/README.md) — classes, structs, interfaces, eventos, propriedades, delegates, operadores/expressões, statements, atributos.
- **C# 1.2:** [MindSetCSharp1_2.Console/Docs/README.md](MindSetCSharp1_2.Console/Docs/README.md) — documento dedicado às alterações (em especial **foreach** + **`IEnumerator.Dispose`**) e os mesmos tópicos base em cópia local.
- **C# 2.0:** [MindSetCSharp2_0.Console/Docs/README.md](MindSetCSharp2_0.Console/Docs/README.md) — genéricos, iteradores, nullable, métodos anónimos, tipos parciais, etc., com narrativa alinhada a **2005 / VS 2005**.
- **C# 3.0:** [MindSetCSharp3_0.Console/Docs/README.md](MindSetCSharp3_0.Console/Docs/README.md) — LINQ, lambdas, extension methods, `var`, expression trees, etc., com narrativa alinhada a **2007–2008 / VS 2008 / .NET 3.5**.
- **C# 4.0:** [MindSetCSharp4_0.Console/Docs/README.md](MindSetCSharp4_0.Console/Docs/README.md) — `dynamic`, argumentos nomeados/opcionais, variança em interfaces, NoPIA, com narrativa alinhada a **2010 / VS 2010 / .NET 4**.
- **C# 5.0:** [MindSetCSharp5_0.Console/Docs/README.md](MindSetCSharp5_0.Console/Docs/README.md) — `async`/`await`, caller info attributes, com narrativa alinhada a **2012 / VS 2012 / .NET 4.5**.
- **C# 7.0:** [MindSetCSharp7_0.Console/Docs/README.md](MindSetCSharp7_0.Console/Docs/README.md) — tuplos, `out var`, pattern matching, `ref`, discards, etc., com narrativa alinhada a **2017 / VS 2017 / .NET Core** *(sem projeto MindSet 6.0)*.
- **C# 7.1:** [MindSetCSharp7_1.Console/Docs/README.md](MindSetCSharp7_1.Console/Docs/README.md) — `async Main`, `default` inferido, tuplos com nomes inferidos, patterns em `T` genérico, `LangVersion`, `-refout` / `-refonly` *(agosto 2017)*.
- **C# 7.2:** [MindSetCSharp7_2.Console/Docs/README.md](MindSetCSharp7_2.Console/Docs/README.md) — `readonly`/`ref struct`, `in`, `ref readonly`, `stackalloc`, `fixed`, `private protected`, … *(novembro 2017)*.
- **C# 7.3:** [MindSetCSharp7_3.Console/Docs/README.md](MindSetCSharp7_3.Console/Docs/README.md) — `unmanaged`, tuplos `==`/`!=`, `[field: …]`, resolução de overload, `-publicsign` / `-pathmap`, … *(maio 2018)*.
- **C# 8.0:** [MindSetCSharp8_0.Console/Docs/README.md](MindSetCSharp8_0.Console/Docs/README.md) — membros `readonly`, default interface members, pattern matching (switch expressions, property/tuple/positional patterns), `using` declarations, funções locais `static`, nullable reference types, `IAsyncEnumerable`, índices e intervalos, `??=`, … *(setembro 2019 / .NET Core 3.0)*.
- **C# 9.0:** [MindSetCSharp9_0.Console/Docs/README.md](MindSetCSharp9_0.Console/Docs/README.md) — *records*, `init`, top-level statements, patterns relacionais e lógicos, `nint`/`nuint`, function pointers, module initializers, `new()` / `?:` com tipo alvo, retornos covariantes, … *(novembro 2020 / .NET 5)*.
- **C# 10.0:** [MindSetCSharp10_0.Console/Docs/README.md](MindSetCSharp10_0.Console/Docs/README.md) — *record structs*, `global using`, *handlers* de interpolação, `namespace` por ficheiro, lambdas melhoradas, `[CallerArgumentExpression]`, … *(novembro 2021 / .NET 6)*.
- **C# 11.0:** [MindSetCSharp11_0.Console/Docs/README.md](MindSetCSharp11_0.Console/Docs/README.md) — *raw strings*, matemática genérica, UTF-8 `u8`, *list patterns*, tipos `file`, `required`, `ref fields` / `scoped`, … *(novembro 2022 / .NET 7)*.
- **C# 12.0:** [MindSetCSharp12_0.Console/Docs/README.md](MindSetCSharp12_0.Console/Docs/README.md) — construtores primários, expressões de coleção, *inline arrays*, lambdas com parâmetros opcionais, `ref readonly`, alias `using` para qualquer tipo, `Experimental`, *interceptors* (pré-visualização), … *(novembro 2023 / .NET 8)*.
- **C# 13.0:** [MindSetCSharp13_0.Console/Docs/README.md](MindSetCSharp13_0.Console/Docs/README.md) — `params` em coleções, `System.Threading.Lock`, `\e`, `ref struct` com interfaces e argumentos de tipo, partial properties/indexers, prioridade de overload, … *(novembro 2024 / .NET 9)*.
- **C# 14.0:** [MindSetCSharp14_0.Console/Docs/README.md](MindSetCSharp14_0.Console/Docs/README.md) — *extension members*, atribuição null-condicional, `nameof` com genéricos não ligados, conversões implícitas `Span`/`ReadOnlySpan`, modificadores em lambdas, propriedades com `field`, partial events/constructors, atribuição composta definida pelo utilizador, … *(novembro 2025 / .NET 10)*.
- **C# 15.0:** [MindSetCSharp15_0.Console/Docs/README.md](MindSetCSharp15_0.Console/Docs/README.md) — argumentos em expressões de coleção (`with(...)`), **.NET 11** (SDK preview / VS 2026 Insiders), …

---

## Contribuição

Projeto mantido pela `dopme-io`. Veja [DOCUMENTATION.md](DOCUMENTATION.md), [EXTENSION_GUIDE.md](EXTENSION_GUIDE.md) e [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Licença

[MIT License](./LICENSE.md).

---

## Contato

- **Email**: [daniloopinheiro@dopme.io](mailto:daniloopinheiro@dopme.io)
- **LinkedIn**: [dopme-io](https://www.linkedin.com/company/dopme-io/)
- **YouTube**: [dopme](https://www.youtube.com/@dopme-io)
- **WhatsApp Business**: [https://wa.me/5511964952665](https://wa.me/5511964952665)

---

*MindSet C# por edição: um console por versão (1.0, 1.2, 2.0, 3.0, 4.0, 5.0, 7.0, 7.1, 7.2, 7.3, 8.0, 9.0, 10.0, …), roteiros em Markdown, pronto para praticar com o SDK atual.*
