# Propriedades com *backing field* (`field`) (C# 14.0)

## Contexto

Em *accessors* de propriedade pode referir-se ao campo de suporte gerado com a palavra-chave **`field`**, em vez de nomes como `_foo` ou `[field: …]` apenas em atributos — simplifica propriedades com lógica em `get`/`set`.

## O que praticar

```csharp
public string Name
{
    get => field;
    set => field = value.Trim();
}
```

Relacione com [attribute-backing-field-auto-properties.md](attribute-backing-field-auto-properties.md) (C# 7.3).

## Próximo passo

[partial-events-constructors.md](partial-events-constructors.md) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
