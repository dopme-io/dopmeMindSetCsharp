# `lock` com `System.Threading.Lock` (C# 13.0)

## Contexto

Se o alvo de **`lock`** for **`System.Threading.Lock`**, o compilador gera código que usa **`Lock.EnterScope()`** para entrar numa secção exclusiva. O **`ref struct`** devolvido segue o padrão **`Dispose()`** para sair do *scope*.

## O que praticar

```csharp
var gate = new System.Threading.Lock();
lock (gate)
{
    // secção exclusiva
}
```

## Próximo passo

[escape-sequence-e.md](escape-sequence-e.md) · [csharp-13-0-overview.md](csharp-13-0-overview.md)
