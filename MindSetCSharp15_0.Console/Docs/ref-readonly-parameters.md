# Parâmetros `ref readonly` (C# 12.0)

## Contexto

**`ref readonly T`** deixa explícito que o argumento é passado por **referência** mas **não deve ser modificado** pelo callee — um meio-termo claro entre **`ref`**, **`in`** e cópia, para desenho de APIs.

## O que praticar

```csharp
static int First(ref readonly int x) => x;
```

Compare com [in-parameter-modifier.md](in-parameter-modifier.md) (C# 7.2) e [ref-locals-returns.md](ref-locals-returns.md) (C# 7).

## Próximo passo

[alias-any-type.md](alias-any-type.md) · [csharp-12-0-overview.md](csharp-12-0-overview.md)
