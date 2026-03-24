# Atributos de informação do chamador (C# 5.0)

## Contexto

Em **C# 5.0**, três atributos em **`System.Runtime.CompilerServices`** permitem que o compilador injete **automaticamente** valores nos parâmetros opcionais da chamada:

- **`[CallerMemberName]`** — nome do membro (método, propriedade, etc.) que chama.
- **`[CallerFilePath]`** — caminho do ficheiro-fonte.
- **`[CallerLineNumber]`** — número da linha na chamada.

Os parâmetros decorados devem ser **opcionais** com valores por defeito **literais** (`null`, `0`, `default`, …) para o compilador poder substituir na **chamada**.

## O que praticar

1. API de log: `void Log(string msg, [CallerMemberName] string? quem = null)` sem o chamador passar `quem`.
2. Combinar com **C# 4.0** [named-optional-arguments.md](named-optional-arguments.md) mentalmente — aqui o compilador preenche, não só o programador.
3. **Não** são substituídos quando o chamador **passa** explicitamente o argumento.

## Exemplo mínimo

```csharp
using System.Runtime.CompilerServices;

static void Rastrear(
    string mensagem,
    [CallerMemberName] string membro = "",
    [CallerFilePath] string ficheiro = "",
    [CallerLineNumber] int linha = 0)
{
    System.Console.WriteLine($"{ficheiro}:{linha} {membro} — {mensagem}");
}

// Rastrear("algo");  // membro, ficheiro, linha preenchidos pelo compilador
```

## Mindset

Útil para **diagnóstico** e **logging** sem reflexão; não substitui um **stack trace** completo em todos os cenários, mas cobre muitos casos simples.

## Próximo passo

[csharp-5-0-overview.md](csharp-5-0-overview.md) (reler) ou tabela **C# 4.0** no [README.md](README.md).
