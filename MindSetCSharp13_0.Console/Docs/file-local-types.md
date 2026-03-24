# Tipos `file` (*file-local*) (C# 11.0)

## Contexto

**`file class Foo`** (ou `struct`, `interface`, `record`, …) restringe o tipo ao **ficheiro de origem** — não é visível fora desse `.cs`. Útil para **código gerado**, helpers internos e evitar poluir o espaço de nomes global.

## O que praticar

```csharp
file static class Helpers
{
    internal static int Twice(int x) => x * 2;
}
```

## Próximo passo

[required-members.md](required-members.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
