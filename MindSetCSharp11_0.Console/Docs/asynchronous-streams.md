# Fluxos assíncronos (`IAsyncEnumerable<T>`) (C# 8.0)

## Ideia

**C# 8.0** introduz **`async`** iteradores: **`yield return`** em métodos assíncronos que devolvem **`IAsyncEnumerable<T>`** / **`IAsyncEnumerator<T>`**, com **`await foreach`** para consumir.

**Dependência de biblioteca:** tipos em **.NET Core 3.0** (e namespaces `System.Collections.Generic` / `System.Threading.Tasks`).

## Exemplo

```csharp
async IAsyncEnumerable<int> ProduceAsync()
{
    await Task.Delay(10);
    yield return 1;
    yield return 2;
}

await foreach (var x in ProduceAsync())
    Console.WriteLine(x);
```

## Mindset

- **Streaming** assíncrono sem carregar coleções inteiras na memória.

## Ver também

- [async-await.md](async-await.md) (C# 5.0)
- [iterators.md](iterators.md) (C# 2.0)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
