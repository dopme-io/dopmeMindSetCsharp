# `stackalloc` em expressões aninhadas (C# 8.0)

## Ideia

**`stackalloc`** pode aparecer em **mais** contextos de expressão (incluindo **aninhados**), não só no topo de uma atribuição direta — alinhado a **`Span<T>`** e código **unsafe** controlado.

## Mindset

- **Menos** variáveis temporárias ao compor buffers na stack.

## Ver também

- [stackalloc-initializers.md](stackalloc-initializers.md) (C# 7.2)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
