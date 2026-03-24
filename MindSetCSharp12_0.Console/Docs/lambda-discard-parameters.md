# Parâmetros de descarte em lambdas (C# 9.0)

## Contexto

Lambdas podem declarar **parâmetros ignorados** com **`_`** (e múltiplos `_` quando necessário), para callbacks cujo contrato exige argumentos que não usa.

## Exemplo

```csharp
Action<int, int> noop = (_, _) => { };
```

## Próximo passo

[attributes-local-functions.md](attributes-local-functions.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
