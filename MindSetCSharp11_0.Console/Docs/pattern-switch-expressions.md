# Expressões `switch` (C# 8.0)

## Ideia

O **`switch`** pode ser usado como **expressão** que devolve um valor: **menos** `break`, **menos** variáveis temporárias, e **exaustividade** verificada quando aplicável.

## Exemplo

```csharp
string label = n switch
{
    0 => "zero",
    1 => "one",
    _ => "many"
};
```

## Mindset

- **Padrão** como valor central; combina com **patterns** em cada ramo.

## Ver também

- [pattern-matching.md](pattern-matching.md) (C# 7.0)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
