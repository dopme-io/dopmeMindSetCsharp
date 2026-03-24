# *Positional patterns* (C# 8.0)

## Ideia

Tipos com **desconstrutor** acessível (ou `Deconstruct`) podem ser correspondidos por **posição**: `(x, y)` no **pattern**, alinhado à ordem de desconstrução.

## Exemplo

```csharp
readonly struct Point
{
    public int X { get; }
    public int Y { get; }
    public Point(int x, int y) { X = x; Y = y; }
    public void Deconstruct(out int x, out int y) { x = X; y = Y; }
}

var p = new Point(3, 4);
if (p is (3, 4))
    Console.WriteLine("match");
```

## Mindset

- Generaliza **tuplos** para **tipos** com `Deconstruct` documentado.

## Ver também

- [pattern-tuple-patterns.md](pattern-tuple-patterns.md)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
