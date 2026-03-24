# Atribuição null-condicional (C# 14.0)

## Contexto

Pode usar-se atribuição **só quando o destino não é null** — por exemplo **`target?.Property = value`** — evitando `if` explícito quando a semântica é “atualizar apenas se existir referência”.

## O que praticar

```csharp
node?.Next = other;
```

Compare com [null-coalescing-assignment.md](null-coalescing-assignment.md) (C# 8) e operador `?.` em [operators-and-expressions.md](operators-and-expressions.md).

## Próximo passo

[nameof-unbound-generic-types.md](nameof-unbound-generic-types.md) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
