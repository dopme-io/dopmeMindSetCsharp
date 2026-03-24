# Pattern matching — início (C# 7.0)

## Contexto

**C# 7.0** deu os primeiros passos em **pattern matching**:

- **`is` com variável**: `if (obj is int i) { usar i }`
- **`switch` com padrões**: `case int n when n < 0:`, `case string s:`, etc.

Versões posteriores (8.0+) acrescentam **property patterns**, **recursive patterns**, `switch` expressions, etc. Aqui focamos o **núcleo 7.0**.

## O que praticar

1. Substituir `var x = obj as string; if (x != null)` por `if (obj is string x)`.
2. `switch (o)` com `case int i:` e **`when`** para condições extra.
3. Combinar com [out-variables.md](out-variables.md) e tuplos onde fizer sentido.

## Exemplo mínimo

```csharp
static string Descrever(object o)
{
    switch (o)
    {
        case null:
            return "nulo";
        case int n when n < 0:
            return "inteiro negativo";
        case int n:
            return "inteiro " + n;
        default:
            return "outro";
    }
}
```

## Mindset

Menos **casts** e ramificações repetitivas; o fluxo fica mais **declarativo** sobre “que forma” tem o valor.

## Próximo passo

[local-functions.md](local-functions.md)
