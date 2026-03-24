# Nomes de elementos de tuplo inferidos (C# 7.1)

## Ideia

Em **C# 7.0**, os tuplos podiam ter **nomes explícitos**: `(int id, string name)`. Em **7.1**, o compilador **infere** frequentemente os nomes dos elementos a partir das **expressões** usadas na inicialização — por exemplo, variáveis cujo nome passa a ser o nome do elemento do tuplo.

## Exemplo

```csharp
int count = 3;
string label = "ok";
var row = (count, label);
// Equivalente conceptual a (count: count, label: label) em muitos contextos
Console.WriteLine(row.count);
Console.WriteLine(row.label);
```

A regra exata evoluiu ligeiramente nas especificações; em caso de dúvida na sua versão, confira a documentação Microsoft ou o compilador (IntelliSense mostra os nomes inferidos).

## Mindset

- **DRY** nos nomes: menos repetição `x: x` quando o nome do membro coincide com a variável.
- Continua a ser válido (e por vezes preferível) **nomear explicitamente** para clareza ou quando a inferência não aplica.

## Ver também

- [tuples-deconstruction.md](tuples-deconstruction.md) (C# 7.0)
- [csharp-7-1-overview.md](csharp-7-1-overview.md)
