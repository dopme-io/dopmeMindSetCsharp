# `private protected` (C# 7.2)

## Ideia

Novo nível de acessibilidade: **`private protected`** significa **acessível** por tipos **derivados**, mas **apenas** na **mesma assembly**. É a interseção de **`protected`** e **`internal`** no sentido restritivo: nem `protected` puro (qualquer assembly) nem `internal` puro (qualquer tipo na assembly).

## Exemplo

```csharp
public class Base
{
    private protected void Hook() { }
}

// Só classes derivadas *nesta* assembly veem Hook().
```

## Mindset

- **Encapsular** extensão por herança **sem** expor API ao resto do mundo.
- Útil em **frameworks** com múltiplas assemblies: hooks **internos** ao conjunto.

## Ver também

- [classes.md](classes.md) (base)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
