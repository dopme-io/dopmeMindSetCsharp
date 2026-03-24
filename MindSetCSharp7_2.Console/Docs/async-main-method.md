# `async` no método `Main` (C# 7.1)

## Ideia

A partir do **C# 7.1**, o **ponto de entrada** da aplicação pode ser **`async`**: o compilador gera o código de arranque que **aguarda** a tarefa devolvida, em vez de obrigar a um `Main` síncrono que chama `.GetAwaiter().GetResult()` (ou padrão semelhante).

## Assinaturas típicas

```csharp
static async Task Main()
{
    await Task.Delay(100);
}

static async Task<int> Main()
{
    await Task.Delay(0);
    return 0;
}
```

Também são admitidas formas com **args** (`string[] args`) quando aplicável à sua versão / compilador.

## Mindset

- **Menos fricção** em consolas e ferramentas que fazem I/O assíncrono logo no arranque.
- O **runtime** continua a precisar de um ponto de entrada válido; o compilador **expande** o `async Main` para algo equivalente e seguro no que toca a exceções não observadas — mantenha boas práticas (`try`/`catch` no topo quando fizer sentido).

## Ver também

- [async-await.md](async-await.md) (C# 5.0) — base de `async`/`await`
- [csharp-7-1-overview.md](csharp-7-1-overview.md)
