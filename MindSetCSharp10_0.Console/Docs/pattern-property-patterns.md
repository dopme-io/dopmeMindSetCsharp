# *Property patterns* (C# 8.0)

## Ideia

Os **patterns** de **C# 8.0** podem corresponder a **propriedades** de um objeto: `{ Prop: pattern }`, encadeando condições sobre a **forma** dos dados.

## Exemplo

```csharp
if (e is MouseEvent { Button: 1 })
    Console.WriteLine("Left click");
```

## Mindset

- Menos **casts** e **null checks** repetidos; pense em **estrutura** do valor.

## Ver também

- [pattern-switch-expressions.md](pattern-switch-expressions.md)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
