# Modificadores em parâmetros de lambdas simples (C# 14.0)

## Contexto

Lambdas com **parâmetros simples** (sem tipo explícito) podem declarar **modificadores** como **`ref`**, **`in`**, **`out`**, quando o contexto do delegado o permite.

## O que praticar

```csharp
delegate void RefInt(ref int x);
RefInt op = (ref int x) => x++;
```

## Próximo passo

[field-backed-properties.md](field-backed-properties.md) · [lambda-explicit-return-type.md](lambda-explicit-return-type.md) (C# 10) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
