# Atribuição de coalescência nula (`??=`) (C# 8.0)

## Ideia

O operador **`??=`** atribui **só se** o lado esquerdo for **null** — evita padrões `if (x == null) x = ...`.

## Exemplo

```csharp
string? cache = null;
cache ??= Compute();
```

## Mindset

- **Inicialização preguiçosa** e caches com menos ruído.

## Ver também

- [csharp-8-0-overview.md](csharp-8-0-overview.md)
