# Atributos genéricos (C# 11.0)

## Contexto

Atributos podem ter **argumentos de tipo**: **`[MyAttribute<T>]`**. Em C# 10 isto era *preview*; em C# 11 integra o conjunto estável da linguagem (com o compilador/SDK suportados).

## O que praticar

```csharp
class TagAttribute<T> : Attribute { }

[Tag<string>]
class Example { }
```

## Próximo passo

[preview-features-csharp-10.md](preview-features-csharp-10.md) (contexto C# 10) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
