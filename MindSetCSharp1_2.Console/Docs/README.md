# C# 1.2 — Roteiro MindSet

**Versão da linguagem:** 1.2  
**Contexto:** abril de 2003, com o **Visual Studio .NET 2003**. C# 1.2 trouxe **melhorias pequenas** sobre a base de C# 1.0; a mais conhecida é o comportamento do **`foreach`**: o código gerado passa a chamar **`Dispose()`** no **`IEnumerator`** quando este implementa **`IDisposable`**, garantindo libertação de recursos ao fim do laço.

Este roteiro usa **.NET e C# atuais** para experimentar; o texto indica o que é próprio da transição **1.0 → 1.2** e o que permanece igual.

## Documento específico C# 1.2

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 0 | **Alterações C# 1.2** (foreach, `IEnumerator`, `Dispose`) | [csharp-1-2-enhancements.md](csharp-1-2-enhancements.md) |

## Base C# 1.0 (ainda válida em 1.2)

Os tópicos abaixo seguem o mesmo enquadramento da edição MindSet C# 1.0; são a fundação sobre a qual 1.2 incide.

| Ordem | Tópico | Ficheiro |
|------:|--------|----------|
| 1 | Classes | [classes.md](classes.md) |
| 2 | Structs | [structs.md](structs.md) |
| 3 | Interfaces | [interfaces.md](interfaces.md) |
| 4 | Eventos | [events.md](events.md) |
| 5 | Propriedades | [properties.md](properties.md) |
| 6 | Delegates | [delegates.md](delegates.md) |
| 7 | Operadores e expressões | [operators-and-expressions.md](operators-and-expressions.md) |
| 8 | Instruções (statements) | [statements.md](statements.md) |
| 9 | Atributos | [attributes.md](attributes.md) |

## Como usar

1. Comece por [csharp-1-2-enhancements.md](csharp-1-2-enhancements.md).
2. Percorra os tópicos 1.0 na ordem que precisar de rever.
3. Execute `dotnet run --project MindSetCSharp1_2.Console` na raiz do repositório (ou a partir da pasta do projeto).

## Ligação ao repositório

- Formato do projeto: [FORMATO_DO_PROJETO.md](../../FORMATO_DO_PROJETO.md)
- Índice geral: [DOCUMENTATION_INDEX.md](../../DOCUMENTATION_INDEX.md)
- Edição C# 1.0: [MindSetCSharp1_0.Console/Docs/README.md](../../MindSetCSharp1_0.Console/Docs/README.md)
- Edições seguintes: [C# 2.0](../../MindSetCSharp2_0.Console/Docs/README.md) · [C# 3.0](../../MindSetCSharp3_0.Console/Docs/README.md) · [C# 4.0](../../MindSetCSharp4_0.Console/Docs/README.md) · [C# 5.0](../../MindSetCSharp5_0.Console/Docs/README.md) · [C# 7.0](../../MindSetCSharp7_0.Console/Docs/README.md) · [C# 7.1](../../MindSetCSharp7_1.Console/Docs/README.md) · [C# 7.2](../../MindSetCSharp7_2.Console/Docs/README.md) · [C# 7.3](../../MindSetCSharp7_3.Console/Docs/README.md) · [C# 8.0](../../MindSetCSharp8_0.Console/Docs/README.md) · [C# 9.0](../../MindSetCSharp9_0.Console/Docs/README.md) · [C# 10.0](../../MindSetCSharp10_0.Console/Docs/README.md)
