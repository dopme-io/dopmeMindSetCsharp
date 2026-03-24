# `ref struct` que implementa interfaces (C# 13.0)

## Contexto

Tipos **`ref struct`** podem **implementar interfaces** (com restrições: sem *boxing* como referência normal, conforme regras da linguagem e do runtime).

## O que praticar

```csharp
ref struct R : IDisposable
{
    public void Dispose() { }
}
```

Relacione com [ref-struct.md](ref-struct.md) (C# 7.2).

## Próximo passo

[ref-struct-type-arguments.md](ref-struct-type-arguments.md) · [csharp-13-0-overview.md](csharp-13-0-overview.md)
