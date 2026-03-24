# Expressões `throw` (C# 7.0)

## Contexto

Antes do C# 7, **`throw`** era sempre uma **instrução**. Em **C# 7.0**, pode aparecer como **expressão** em contextos onde uma expressão é obrigatória — por exemplo:

- Operador **null-coalescing**: `return arg ?? throw new ArgumentNullException(nameof(arg));`
- Operador **ternário** (com cuidado na legibilidade).

Isto reduz verificações `if (arg == null) throw …` repetidas.

## O que praticar

1. `var x = cache ?? throw new InvalidOperationException("cache vazio");`
2. Combinar com **`nameof`** (C# 6) em mensagens de exceção.
3. Não substituir **toda** a validação por `throw` embutido se prejudicar a leitura.

## Exemplo mínimo

```csharp
static string ExigirTexto(string? s)
{
    return s ?? throw new System.ArgumentNullException(nameof(s));
}
```

## Mindset

**Invariantes** expressos de forma **compacta** na expressão principal.

## Próximo passo

[csharp-7-0-overview.md](csharp-7-0-overview.md) (reler) ou [README.md](README.md)
