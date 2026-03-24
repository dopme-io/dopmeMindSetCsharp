# Instruções — statements (C# 1.0)

## Contexto

**Statements** estruturam o fluxo do programa: declarações locais, atribuições, chamadas, `if`/`else`, `switch`, laços (`for`, `while`, `do`/`while`, `foreach` em arrays e `IEnumerable` clássico), `break`/`continue`/`return`, `try`/`catch`/`finally`/`throw`, `using` com `IDisposable` (introduzido na primeira geração do C# com .NET), `lock` para exclusão mútua, etc.

> **C# 1.2:** a partir do VS .NET 2003, o `foreach` passa a chamar `Dispose()` em `IEnumerator` que implementa `IDisposable`. Ver [csharp-1-2-enhancements.md](csharp-1-2-enhancements.md).

## O que implementar / praticar

1. **`foreach`**: percorrer `array` ou coleção que implemente `IEnumerable` / `IEnumerator` (em 1.0/1.2, sem genéricos). Com 1.2+, pense em `Dispose` no enumerador quando houver recursos.
2. **`switch`**: ramificar por valores constantes; `goto case` existe mas use com extrema moderação.
3. **Exceções**: capturar tipos específicos; não esvaziar `catch` sem relogar ou rethrow consciente.
4. **`using`**: garantir `Dispose()` em recursos mesmo com exceção.

## Exemplo mínimo — try / finally (padrão antes de `using` generalizado)

```csharp
public static void EscreverFicheiroSimulado()
{
    System.IO.StreamWriter? w = null;
    try
    {
        w = new System.IO.StreamWriter("exemplo.txt");
        w.WriteLine("Olá, C# 1.0 mindset.");
    }
    finally
    {
        if (w != null)
        {
            ((System.IDisposable)w).Dispose();
        }
    }
}
```

(Com C# moderno, prefira `using var w = ...`.)

## Exemplo — `foreach` em array

```csharp
int[] nums = { 1, 2, 3 };
foreach (int n in nums)
{
    System.Console.WriteLine(n);
}
```

## Mindset

- Cada ramo (`if`/`switch`) deve ser **legível** e **exaustivo** nos casos de negócio.
- Exceções para **situações excecionais**, não para fluxo normal.

## Próximo passo

[attributes.md](attributes.md) — metadados declarativos sobre tipos e membros.
