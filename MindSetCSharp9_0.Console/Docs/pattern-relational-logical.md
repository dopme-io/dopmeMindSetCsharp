# Patterns relacionais e lógicos (C# 9.0)

## Contexto

Os **patterns** ganham **operadores relacionais** em tipos numéricos (`<`, `>`, `<=`, `>=`) e **combinações lógicas**: **`and`**, **`or`**, **`not`**, com **parênteses** para precedência. Há também **type patterns** (`x is T t`) em mais contextos.

O idioma **`e is not null`** torna-se natural para testes de não nulidade em qualquer sítio onde patterns são válidos (`is`, `switch` expression, `case`, patterns aninhados).

## Exemplos

```csharp
static string Classificar(int n) => n switch
{
    < 0 => "negativo",
    0 => "zero",
    > 0 and < 10 => "pequeno positivo",
    _ => "outro"
};

if (e is not null)
{
    // e tratado como não nulo no fluxo (com NRT)
}
```

## Próximo passo

[pattern-switch-expressions.md](pattern-switch-expressions.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
