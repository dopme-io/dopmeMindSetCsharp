# Genéricos (C# 2.0)

## Contexto

**Genéricos** permitem declarar **parâmetros de tipo** em classes, structs, interfaces e métodos. O código é compilado de forma **type-safe** sem depender de `object` e casts em todo o lado.

## O que implementar / praticar

1. Criar uma classe simples `Caixa<T>` que guarda um valor tipado.
2. Usar **`List<T>`**, **`Dictionary<TKey,TValue>`** do .NET em vez de coleções não genéricas quando fizer sentido.
3. Restringir tipos com **`where T : class`**, **`where T : struct`**, **`new()`**, interface, etc., quando precisar de garantias.

## Exemplo mínimo

```csharp
public sealed class Par<TPrimeiro, TSegundo>
{
    public TPrimeiro Primeiro { get; }
    public TSegundo Segundo { get; }

    public Par(TPrimeiro primeiro, TSegundo segundo)
    {
        Primeiro = primeiro;
        Segundo = segundo;
    }
}

// Uso
var p = new Par<string, int>("idade", 30);
```

## Porquê melhor que `ArrayList`

- Sem **boxing** desnecessário para tipos valor.
- Erros de tipo aparecem no **compilador**, não só em runtime.

## Próximo passo

[partial-types.md](partial-types.md)
