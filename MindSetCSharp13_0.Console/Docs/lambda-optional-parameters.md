# Parâmetros opcionais em lambdas (C# 12.0)

## Contexto

Expressões lambda podem declarar **valores por omissão** nos parâmetros, como em métodos normais — **`(int x = 0) => …`**.

## O que praticar

```csharp
Func<int, int, int> add = (a, b = 1) => a + b;
```

Relacione com [lambda-explicit-return-type.md](lambda-explicit-return-type.md) (C# 10).

## Próximo passo

[ref-readonly-parameters.md](ref-readonly-parameters.md) · [csharp-12-0-overview.md](csharp-12-0-overview.md)
