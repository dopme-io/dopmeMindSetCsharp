# Métodos parciais (C# 3.0)

## Contexto

Com **tipos parciais** (C# 2.0, ver [partial-types.md](partial-types.md)), C# 3.0 acrescentou **métodos parciais**: declarados numa parte da classe com **`partial void Nome();`** e **opcionalmente** implementados noutra parte. Se não houver implementação, o compilador **remove** a declaração e as chamadas — custo zero em runtime.

Útil para **geradores de código** (ex.: Designer) que injetam ganchos sem forçar implementação vazia em todo o projeto.

## O que praticar

1. Declaração num partial: `partial void OnAlterado();`
2. Implementação noutro ficheiro partial da mesma classe.
3. Métodos parciais devem ser **`void`**, tipicamente **privados**, e não podem ser **virtuais** da forma habitual.

## Exemplo mínimo

```csharp
public partial class Modelo
{
    partial void OnValidado();

    public void Validar()
    {
        // …
        OnValidado();
    }
}

public partial class Modelo
{
    partial void OnValidado()
    {
        // lógica opcional
    }
}
```

## Mindset

**Extensibilidade** sem poluir API pública; o compilador elimina chamadas se não existir implementação.

## Próximo passo

[csharp-3-0-overview.md](csharp-3-0-overview.md) (reler enquadramento) ou [csharp-2-0-overview.md](csharp-2-0-overview.md) para a camada anterior.
