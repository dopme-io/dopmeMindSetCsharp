# Delegates (C# 1.0)

## Contexto

Um **delegate** é um **tipo** que representa referências a métodos com uma assinatura fixa. Em C# 1.0, eram a base de **eventos**, callbacks e padrões como `BeginInvoke` / `EndInvoke` na programação assíncrona da época (muito mais verbosa que `async/await`).

## O que implementar / praticas

1. Declarar `delegate void Operacao(int x);` (ou outro retorno/parâmetros).
2. Atribuir **métodos nomeados** compatíveis com a assinatura.
3. **Multicast**: `a + b` combina invocações; `a - b` remove (cuidado com referências nulas).

## Exemplo mínimo

```csharp
public delegate int Binario(int a, int b);

public static class DemoDelegates
{
    public static void Executar()
    {
        Binario op = Somar;
        op += Multiplicar; // multicast: na prática o último retorno “ganha” se usar o valor de retorno

        int r = op(3, 4);
        System.Console.WriteLine(r);
    }

    private static int Somar(int a, int b) { return a + b; }
    private static int Multiplicar(int a, int b) { return a * b; }
}
```

Para **eventos**, prefira `EventHandler` ou um delegate dedicado com `sender` e `EventArgs`.

## Mindset

- Delegate = **contrato de chamada**: quem invoca não precisa saber a implementação exata.
- Multicast é poderoso mas exige clareza sobre **ordem** e **valor de retorno**.

## O que veio depois

**Delegates anónimos** (C# 2.0), **lambdas** (C# 3.0+), `Func<>`/`Action<>` (genéricos, C# 2.0+).

## Próximo passo

[operators-and-expressions.md](operators-and-expressions.md) — expressões que combinam valores e tipos.
