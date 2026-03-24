# Pattern matching em parâmetros de tipo genérico (C# 7.1)

## Ideia

Em **C# 7.0**, o uso de **`is`** com **introdução de variável** (`e is int i`) era **limitado** quando o operando era uma **variável cujo tipo era um parâmetro de tipo** `T` — o compilador não podia assumir que `T` fosse um tipo concreto compatível com o pattern.

**C# 7.1** alargou as regras para permitir **pattern matching** em expressões cujo tipo estático é um **parâmetro de tipo genérico** (com as restrições e avisos que o compilador impõe).

## Exemplo ilustrativo

```csharp
static void Describe<T>(T value)
{
    if (value is int i)
        Console.WriteLine($"Inteiro: {i}");
    else if (value is string s)
        Console.WriteLine($"Texto: {s}");
    else
        Console.WriteLine("Outro");
}
```

O compilador trata `T` como potencialmente **qualquer** tipo; os *patterns* aplicam-se em tempo de execução com as conversões/unboxing habituais.

## Mindset

- Útil em **APIs genéricas** (helpers, serialização, visitantes) sem forçar `object` intermédio só para poder usar `is`.
- Tenha atenção ao **custo** e à **clareza**: muitas ramificações sobre `T` podem indicar necessidade de **restrições** (`where T : …`) ou de **polimorfismo** em vez de cadeias de `is`.

## Ver também

- [pattern-matching.md](pattern-matching.md) (C# 7.0)
- [generics.md](generics.md) (C# 2.0)
- [csharp-7-1-overview.md](csharp-7-1-overview.md)
