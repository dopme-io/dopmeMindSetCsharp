# *Record structs* (C# 10.0)

## Contexto

**`record struct`** (e a forma `readonly record struct`) oferece tipos valor com **sintaxe de record** — muitos membros sintetizados como em *record class*, com semântica de **tipo valor**.

## O que praticar

```csharp
public readonly record struct Point(int X, int Y);

var p = new Point(1, 2);
var q = p with { Y = 3 };
```

Compare com [records.md](records.md) (C# 9, tipos referência).

## Próximo passo

[structure-types-improvements.md](structure-types-improvements.md) · [csharp-10-0-overview.md](csharp-10-0-overview.md)
