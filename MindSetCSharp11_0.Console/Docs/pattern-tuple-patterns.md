# *Tuple patterns* (C# 8.0)

## Ideia

Os **patterns** podem corresponder a **tuplos** diretamente, alinhando a sintaxe de **desconstrução** com ramos de `switch`/`is`.

## Exemplo

```csharp
string Describe((int x, int y) p) => p switch
{
    (0, 0) => "origin",
    (_, 0) => "on X axis",
    _ => "other"
};
```

## Mindset

- **Coordenadas** e **pares** de valores como casos de primeira classe.

## Ver também

- [tuples-deconstruction.md](tuples-deconstruction.md) (C# 7.0)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
