# `ref struct` (C# 7.2)

## Ideia

**`ref struct`** declara um tipo de valor que **deve** viver na **stack** (não pode ser campo de classe normal, boxed, etc., segundo as regras). Foi desenhado para tipos como **`Span<T>`** que **referenciam** buffers geridos ou stack sem cópia de heap desnecessária.

## Exemplo

```csharp
ref struct OnlyStack
{
    public Span<byte> Slice;
}
```

(Regras exatas evoluem; o compilador **restringe** usos inválidos.)

## Mindset

- **Representação** de **janelas** sobre memória com **custo** previsível.
- Erros de compilação em usos proibidos são **preferíveis** a corrupção silenciosa de memória.

## Ver também

- [stackalloc-initializers.md](stackalloc-initializers.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
