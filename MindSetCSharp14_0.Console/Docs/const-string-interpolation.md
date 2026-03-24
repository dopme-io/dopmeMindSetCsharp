# Interpolação em `const string` (C# 10.0)

## Contexto

Se **todos** os placeholders forem **cadeias constantes**, pode usar **`$"..."`** na inicialização de **`const string`** — o resultado é calculado em **tempo de compilação**.

```csharp
const string A = "a";
const string B = $"{A}b"; // válido quando as partes são const
```

## Próximo passo

[record-tostring-sealed.md](record-tostring-sealed.md) · [csharp-10-0-overview.md](csharp-10-0-overview.md)
