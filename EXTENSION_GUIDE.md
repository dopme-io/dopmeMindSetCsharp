# Guia de extensão — roteiros MindSet (Docs/)

## Acrescentar um documento em `Docs/`

1. Escolha a edição (ex.: `MindSetCSharp1_0.Console`, …, `MindSetCSharp10_0.Console`).
2. Crie `…/Docs/seu-topico.md` (minúsculas e hífens, ex.: `namespaces.md`).
3. Inclua:
   - **Contexto** (ligação à versão C# / Visual Studio da edição).
   - **O que implementar / praticar** (passos mindset).
   - **Exemplo mínimo** em C# (SDK moderno permitido; indique diferenças históricas).
   - **Mindset — perguntas** ou **Próximo passo** com link para outro `.md`.
4. Atualize a tabela em `Docs/README.md` dessa edição.
5. Opcional: [DOCUMENTATION_INDEX.md](DOCUMENTATION_INDEX.md).

## Acrescentar código de demonstração

- Ficheiros `.cs` extra no mesmo projeto console (ex.: `Demos/…`) e chamadas a partir de `Program.cs`.
- Mantenha exemplos **pequenos** e alinhados ao documento.

## Nova edição console (ex.: C# 11.0)

1. Copie a estrutura de `MindSetCSharp10_0.Console` ou de uma edição anterior (`Program.cs` + `Docs/`).
2. Ajuste `RootNamespace`, nome do `.csproj` e conteúdo dos guias.
3. `dotnet sln add` e atualize [FORMATO_DO_PROJETO.md](FORMATO_DO_PROJETO.md) e [README.md](README.md).
