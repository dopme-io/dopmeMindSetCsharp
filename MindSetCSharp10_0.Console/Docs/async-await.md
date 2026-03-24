# Membros assíncronos — `async` e `await` (C# 5.0)

## Contexto

Com **`async`** e **`await`**, métodos, propriedades com `get` assíncrono (em versões posteriores), **lambdas** e **anónimos** podem consumir operações baseadas em **`Task`** / **`Task<T>`** (padrão TAP — *Task-based Asynchronous Pattern*) sem bloquear desnecessariamente a thread que está a executar o código **entre** os pontos de `await`.

O compilador transforma o método `async` numa **máquina de estados**: cada `await` regista uma continuação; quando a operação completa, a execução **retoma** a partir desse ponto.

## O que praticar

1. Assinaturas: `async Task FooAsync()` e `async Task<int> ComputeAsync()`.
2. **`await`**: só dentro de métodos **`async`** (com exceções raras como `async void` em *event handlers* — usar com cuidado).
3. **Exceções**: erros em `Task` assíncronos propagam-se ao **aguardar** a tarefa; trate com `try`/`catch` em torno de `await` quando fizer sentido.
4. **UI / ASP.NET**: históricamente, libertar o thread de UI ou threads de pedido; em código novo, continue a evitar **`.Result`** / **`.Wait()`** em contextos que podem causar **deadlock** (especialmente com contextos de sincronização capturados).

## Exemplo mínimo

```csharp
using System.Threading.Tasks;

static async Task<int> ObterTamanhoAsync()
{
    await Task.Delay(10); // simula I/O ou trabalho assíncrono
    return 42;
}
```

## Mindset

Pense em **operações** que **demoram** (rede, disco, filas) como candidatas a `async`; CPU pura e pesada pode precisar de **`Task.Run`** ou outros modelos — não confunda “async” com “paralelismo em todas as linhas”.

## Próximo passo

[caller-info-attributes.md](caller-info-attributes.md)
