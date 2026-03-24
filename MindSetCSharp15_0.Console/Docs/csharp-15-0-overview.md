# C# 15.0 — visão geral

## Contexto

**C# 15** é a versão mais recente da linguagem, com suporte em **.NET 11**. Para experimentar as novidades use o **SDK .NET 11 (preview)** ou o **Visual Studio 2026 Insiders** (inclui o preview SDK).

- **Versionamento:** ver documentação Microsoft sobre *C# language versioning*.  
- **Novidades:** a página *What's new in C#* é atualizada quando as funcionalidades entram em pré-visualização pública.  
- **Estado no compilador:** a secção *working set* da página de estado de funcionalidades do **Roslyn** indica quando os *merges* chegam ao ramo principal.  
- **Breaking changes:** artigo dedicado da Microsoft.  
- **Feedback:** problemas com funcionalidades novas → *issue* em **dotnet/roslyn**.

O projeto **MindSetCSharp15_0.Console** usa **`LangVersion` `preview`** no `.csproj` enquanto o SDK instalado não expõe **`15`** como valor explícito; com **SDK .NET 11** (C# 15), altere para **`<LangVersion>15</LangVersion>`**.

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| Argumentos em expressões de coleção (`with(...)`) | [collection-expression-arguments.md](collection-expression-arguments.md) |

Relacione com expressões de coleção em C# 12: [collection-expressions.md](collection-expressions.md).

## Edições anteriores na mesma pasta

Guias **14.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[collection-expression-arguments.md](collection-expression-arguments.md)
