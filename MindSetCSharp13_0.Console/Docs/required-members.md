# Membros `required` (C# 11.0)

## Contexto

O modificador **`required`** em propriedades (e campos públicos aplicáveis) obriga o **inicializador de objeto** ou construtor a **definir** esses membros; o compilador emite erro se faltar.

## O que praticar

```csharp
public class Options
{
    public required string Name { get; init; }
}

// var o = new Options(); // erro
var ok = new Options { Name = "x" };
```

## Próximo passo

[auto-default-structs.md](auto-default-structs.md) · [init-only-setters.md](init-only-setters.md) (C# 9) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
