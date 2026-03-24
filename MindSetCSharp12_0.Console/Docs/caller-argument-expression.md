# `[CallerArgumentExpression]` (C# 10.0)

## Contexto

Semelhante aos atributos *caller info*, **`CallerArgumentExpression`** injeta a **expressão de código fonte** do argumento — útil para APIs de **validação** e mensagens sem repetir strings.

```csharp
static void Require(bool condition, [CallerArgumentExpression(nameof(condition))] string? expr = null)
{
    if (!condition) throw new InvalidOperationException(expr);
}
```

## Próximo passo

[line-pragma-csharp-10.md](line-pragma-csharp-10.md) · [caller-info-attributes.md](caller-info-attributes.md)
