# Membros `readonly` (C# 8.0)

## Ideia

Em **structs**, pode marcar **membros** (métodos, propriedades, indexadores) com **`readonly`** para indicar que **não modificam** o estado da instância. O compilador **restringe** escrita acidental a campos e ajuda a **otimizar** cópias defensivas.

## Exemplo

```csharp
struct Counter
{
    private int _count;

    public readonly int Total => _count;

    public readonly int Peek() => _count;
}
```

## Mindset

- **Imutabilidade** explícita em APIs de structs.
- Alinha com **`in`** e **`readonly struct`** de versões anteriores.

## Ver também

- [readonly-struct.md](readonly-struct.md) (C# 7.2)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
