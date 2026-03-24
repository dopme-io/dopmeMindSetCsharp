# Métodos de extensão (C# 3.0)

## Contexto

**Métodos de extensão** são métodos `static` numa classe `static`, com o **primeiro parâmetro** prefixado por **`this`**. O compilador permite chamá-los como se fossem métodos de instância no tipo do primeiro parâmetro.

O **LINQ** em `System.Linq` baseia-se fortemente neles (`Where`, `Select`, `Average`, …) sobre `IEnumerable<T>` e tipos relacionados.

## O que praticar

1. Definir um método de extensão num namespace e **importar** com `using` para ativar a sintaxe de extensão.
2. `list.Average()` em `List<int>` após `using System.Linq;`.
3. Resolução: métodos de instância **ganham** sobre extensões; extensões importadas podem colidir — cuide dos `using`.

## Exemplo mínimo (C# 3.0)

```csharp
public static class StringExtras
{
    public static bool IsNullOrEmpty(this string s)
    {
        return string.IsNullOrEmpty(s);
    }
}
```

## Mindset

Estender tipos **sem** herança nem alterar o tipo original — poderoso para **APIs fluentes** e LINQ; abuso pode espalhar “mágica” por `using`.

## Próximo passo

[query-expressions-linq.md](query-expressions-linq.md)
