# `readonly struct` (C# 7.2)

## Ideia

Marque um **`struct`** com **`readonly`** para indicar que **todos** os membros de instância são **somente leitura** e que o tipo deve ser tratado como **imutável**. O compilador pode **copiar** e **passar** o valor de forma mais eficiente (por exemplo, com **`in`**) e reforça a intenção de design.

## Exemplo

```csharp
readonly struct Point
{
    public readonly int X;
    public readonly int Y;
    public Point(int x, int y) { X = x; Y = y; }
}
```

## Mindset

- **Semântica clara**: "este valor não muda após construção" (salvo `ref`/`unsafe` fora do modelo).
- Alinha com **`in`** e **`ref readonly`** para APIs de baixa alocação.

## Ver também

- [in-parameter-modifier.md](in-parameter-modifier.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
