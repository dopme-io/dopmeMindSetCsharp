# *Setters* só `init` (C# 9.0)

## Contexto

Propriedades podem usar **`init`** em vez de `set`: só podem ser atribuídas no **construtor** ou num **inicializador de objecto** na criação. Combinam bem com **records** e **imutabilidade** aparente, permitindo **expressões `with`** para criar variantes sem alterar a instância original.

## Exemplo mínimo

```csharp
public record Config(string AppId)
{
    public string Ambiente { get; init; } = "dev";
}

var x = new Config("app1") { Ambiente = "prod" };
// x.Ambiente = "dev"; // erro: init fora do construtor/inicializador
```

## Próximo passo

[records.md](records.md) · [pattern-relational-logical.md](pattern-relational-logical.md)
