# Operadores e expressões (C# 1.0)

## Contexto

**Expressões** produzem valores; **operadores** combinam operandos (`+`, `&&`, `new`, `is`, `as`, etc.). C# 1.0 já tinha operadores aritméticos, lógicos, de comparação, atribuição, condicional ternário (`?:`), `new`, acesso a membros, indexação em arrays, conversões implícitas/explícitas e operadores definidos pelo utilizador (`operator +`, etc.).

## O que implementar / praticar

1. **Precedência e associatividade**: usar parênteses quando a intenção não for óbvia.
2. **Curto-circuito**: `&&` e `||` não avaliam o segundo operando se não for necessário.
3. **`is` / `as`**: teste e conversão segura de tipos referência (padrão clássico antes de padrões modernos).
4. **Sobrecarga**: só onde melhora a leitura (ex.: `Vector` + `Vector`).

## Exemplo mínimo — `is` e `as`

```csharp
public static void Descrever(object o)
{
    if (o is string)
    {
        string s = (string)o;
        System.Console.WriteLine("Texto: " + s);
        return;
    }

    string? comoTexto = o as string;
    if (comoTexto != null)
    {
        System.Console.WriteLine("Também texto: " + comoTexto);
    }
}
```

(Em C# 1.0 não havia `string?`; use `string` e compare com `null`.)

## Exemplo — operador definido pelo utilizador

```csharp
public struct Fracao
{
    public int Numerador;
    public int Denominador;

    public static Fracao operator +(Fracao a, Fracao b)
    {
        return new Fracao
        {
            Numerador = a.Numerador * b.Denominador + b.Numerador * a.Denominador,
            Denominador = a.Denominador * b.Denominador
        };
    }
}
```

## Mindset

- Operador sobrecarregado deve manter **intuição matemática** ou de domínio.
- `as` + verificação de `null` evita **exceção** desnecessária frente a `cast` direto.

## Próximo passo

[statements.md](statements.md) — fluxo de controlo e instruções imperativas.
