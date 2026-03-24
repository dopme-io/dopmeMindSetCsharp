# `GetEnumerator` de extensão e `foreach` (C# 9.0)

## Contexto

Se um tipo **não** implementa `GetEnumerator` mas existe um **método de extensão** `GetEnumerator()` aplicável, o **`foreach`** pode usá-lo — o mesmo padrão que já existia para `await` e `GetAwaiter`.

## Exemplo

```csharp
public readonly struct MyCollection
{
    public readonly int[] Data;
    public MyCollection(int[] d) => Data = d;
}

public static class MyCollectionExt
{
    public static IEnumerator<int> GetEnumerator(this MyCollection c)
    {
        for (int i = 0; i < c.Data.Length; i++)
            yield return c.Data[i];
    }
}

// foreach (var x in new MyCollection(new[] { 1, 2, 3 })) { ... }
```

`MyCollection` não precisa de implementar `IEnumerable<T>`; o `foreach` usa o `GetEnumerator` de extensão.

## Próximo passo

[lambda-discard-parameters.md](lambda-discard-parameters.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
