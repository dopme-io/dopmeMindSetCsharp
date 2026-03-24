# Checklist de validação — MindSetCSharp

## Solução

- [ ] `MindSetCSharp.sln` inclui os projetos console previstos (`MindSetCSharp1_0.Console`, `MindSetCSharp1_2.Console`, `MindSetCSharp2_0.Console`, `MindSetCSharp3_0.Console`, `MindSetCSharp4_0.Console`, `MindSetCSharp5_0.Console`, `MindSetCSharp7_0.Console`, `MindSetCSharp7_1.Console`, `MindSetCSharp7_2.Console`, `MindSetCSharp7_3.Console`, `MindSetCSharp8_0.Console`, `MindSetCSharp9_0.Console`, `MindSetCSharp10_0.Console`, …).

## Edição C# 1.0

- [ ] `MindSetCSharp1_0.Console/Docs/README.md` com tabela dos nove tópicos.
- [ ] Ficheiros: `classes.md` … `attributes.md`.
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 1.2

- [ ] `MindSetCSharp1_2.Console/Docs/README.md` com entrada **csharp-1-2-enhancements.md** e tabela base 1.0.
- [ ] Existe `csharp-1-2-enhancements.md` (foreach, `IEnumerator`, `Dispose`).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 2.0

- [ ] `MindSetCSharp2_0.Console/Docs/README.md` com tabela **C# 2.0** e base 1.0.
- [ ] Existem `csharp-2-0-overview.md` e guias associados (`generics.md`, `iterators.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 3.0

- [ ] `MindSetCSharp3_0.Console/Docs/README.md` com tabela **C# 3.0** e referência a 2.0 / 1.0.
- [ ] Existem `csharp-3-0-overview.md` e guias associados (`query-expressions-linq.md`, `lambda-expressions.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 4.0

- [ ] `MindSetCSharp4_0.Console/Docs/README.md` com tabela **C# 4.0** e referência a 3.0 / 2.0 / 1.0.
- [ ] Existem `csharp-4-0-overview.md` e guias associados (`dynamic-binding.md`, `generic-variance-interfaces.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 5.0

- [ ] `MindSetCSharp5_0.Console/Docs/README.md` com tabela **C# 5.0** e referência às edições anteriores na mesma pasta.
- [ ] Existem `csharp-5-0-overview.md`, `async-await.md`, `caller-info-attributes.md`.
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 7.0

- [ ] `MindSetCSharp7_0.Console/Docs/README.md` com tabela **C# 7.0** e referência **5.0** … **1.0**.
- [ ] Existem `csharp-7-0-overview.md` e guias associados (`out-variables.md`, `tuples-deconstruction.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 7.1

- [ ] `MindSetCSharp7_1.Console/Docs/README.md` com tabela **C# 7.1** e guias **7.0** … em cópia.
- [ ] Existem `csharp-7-1-overview.md` e guias associados (`async-main-method.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 7.2

- [ ] `MindSetCSharp7_2.Console/Docs/README.md` com tabela **C# 7.2** e guias **7.1**/**7.0**/… em cópia.
- [ ] Existem `csharp-7-2-overview.md` e guias associados (`readonly-struct.md`, `ref-struct.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 7.3

- [ ] `MindSetCSharp7_3.Console/Docs/README.md` com tabela **C# 7.3** e guias **7.2**/… em cópia.
- [ ] Existem `csharp-7-3-overview.md` e guias associados (`generic-constraint-unmanaged.md`, `tuple-equality-operators.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 8.0

- [ ] `MindSetCSharp8_0.Console/Docs/README.md` com tabela **C# 8.0** e guias **7.3**/… em cópia.
- [ ] Existem `csharp-8-0-overview.md` e guias associados (`readonly-members.md`, `nullable-reference-types.md`, `asynchronous-streams.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 9.0

- [ ] `MindSetCSharp9_0.Console/Docs/README.md` com tabela **C# 9.0** e guias **8.0**/… em cópia.
- [ ] Existem `csharp-9-0-overview.md` e guias associados (`records.md`, `pattern-relational-logical.md`, `top-level-statements.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Edição C# 10.0

- [ ] `MindSetCSharp10_0.Console/Docs/README.md` com tabela **C# 10.0** e guias **9.0**/… em cópia.
- [ ] Existem `csharp-10-0-overview.md` e guias associados (`record-structs.md`, `global-usings.md`, `interpolated-string-handlers.md`, …).
- [ ] `Program.cs` aponta para `Docs/README.md`.

## Geral

- [ ] Sem pastas legadas (`Pipeline/`, `Produtivo/`, …).
- [ ] [README.md](README.md) e [DOCUMENTATION.md](DOCUMENTATION.md) listam todas as edições.

## Build

```powershell
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
```
