# C# 3.0 — visão geral (final de 2007)

## Contexto

**C# 3.0** chegou com o **Visual Studio 2008** (final de **2007**). O conjunto completo de funcionalidades alinhou-se sobretudo com o **.NET Framework 3.5**. Esta versão marcou um salto na maturidade da linguagem: C# consolidou-se como ferramenta **muito expressiva** para dados e coleções.

A funcionalidade de maior impacto foi o **LINQ** — *Language-Integrated Query* — através das **expressões de consulta** (sintaxe semelhante a SQL) e dos **métodos de extensão** em `System.Linq`. Em vez de um `for` manual para, por exemplo, calcular a **média** de uma lista de inteiros, torna-se natural escrever algo como **`list.Average()`** (desde que exista o método de extensão adequado sobre o tipo enumerável).

## Fundação do LINQ

Uma leitura mais fina coloca **árvores de expressão** (`Expression<T>`), **expressões lambda** e **tipos anónimos** como alicerces sobre os quais o LINQ se apoia. Em qualquer dos casos, C# 3.0 introduziu uma ideia forte: misturar **orientação a objetos** com um estilo mais **declarativo e funcional** (consultas sobre sequências, projeções, composição).

## O que este roteiro cobre

Os documentos em `Docs/` detalham cada área. Use o **SDK .NET atual** para experimentar; as notas assinalam o que é próprio de **3.0** e o que evoluiu depois (ex.: **async/await** é bem mais tarde).

## Mindset

- **Declarativo**: dizer *o quê* quer filtrar ou projetar, e deixar biblioteca e compilador ajudarem no *como*.
- **Composição**: lambdas, inicializadores e extension methods encaixam-se para código mais curto e legível — desde que o time concorde com o nível de “magia”.

## Próximo passo

[implicitly-typed-locals-var.md](implicitly-typed-locals-var.md) (muitos exemplos 3.0 usam `var`) ou, se preferir ir direto ao núcleo: [query-expressions-linq.md](query-expressions-linq.md).
