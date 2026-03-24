# C# 1.2 — alterações da linguagem (abril 2003)

## Contexto

**C# 1.2** acompanhou o **Visual Studio .NET 2003**. As mudanças foram **pontuais** em relação a C# 1.0; a mais citada na documentação histórica é o comportamento do **`foreach`**.

## O que mudou (foreach e `Dispose`)

A partir de C# 1.2, o código gerado para **`foreach`** garante que, se o **`IEnumerator`** devolvido pela coleção implementar **`IDisposable`**, é chamado **`Dispose()`** no fim do laço (em geral via `try`/`finally` gerado pelo compilador), inclusive ao sair por **`break`** ou quando uma exceção atravessa o laço.

**Porquê importa**

- Enumeradores que envolvem recursos (handles, streams, etc.) podem libertá-los de forma determinística.
- Alinha o `foreach` com o padrão **`IDisposable`** da plataforma .NET.

## Comportamento mental (mindset)

1. Se implementar **`IEnumerator`** manualmente e gerir recursos, faça o enumerador implementar **`IDisposable`** quando fizer sentido — com compilador ≥ 1.2, quem usa **`foreach`** beneficia de **`Dispose`** automático.
2. **`IEnumerable.GetEnumerator()`** deve devolver o enumerador que “dona” do recurso, ou um objeto que delegue **`Dispose`** corretamente.

## Exemplo mínimo (estilo C# 1.0 / 1.2)

```csharp
using System;
using System.Collections;

public sealed class DisposableEnumerator : IEnumerator, IDisposable
{
    private int _indice = -1;
    private readonly int[] _dados;

    public DisposableEnumerator(int[] dados)
    {
        _dados = dados;
    }

    public bool MoveNext()
    {
        _indice++;
        return _indice < _dados.Length;
    }

    public void Reset()
    {
        _indice = -1;
    }

    public object Current
    {
        get
        {
            if (_indice < 0 || _indice >= _dados.Length)
                throw new InvalidOperationException();
            return _dados[_indice];
        }
    }

    public void Dispose()
    {
        Console.WriteLine("Dispose() do enumerador.");
    }
}

public sealed class Numeros : IEnumerable
{
    private readonly int[] _itens;

    public Numeros(int[] itens)
    {
        _itens = itens;
    }

    public IEnumerator GetEnumerator()
    {
        return new DisposableEnumerator(_itens);
    }
}
```

Uso:

```csharp
var c = new Numeros(new int[] { 10, 20, 30 });
foreach (object x in c)
{
    Console.WriteLine(x);
}
// Ao terminar o foreach, o compilador (1.2+) chama Dispose no IEnumerator.
```

Nota: **`yield return`**, **`IEnumerable<T>`** e outros atalhos são **posteriores** a 1.2; aqui o objetivo é ver **`IEnumerator` + `IDisposable` + `foreach`**.

## Relação com [statements.md](statements.md)

O documento sobre **statements** cobre `foreach` de forma geral; este ficheiro fixa a **evolução 1.0 → 1.2** nesse ponto.

## Mindset — perguntas

- O enumerador da sua coleção mantém estado que **deve** ser libertado?
- Sem `Dispose` automático no `foreach`, onde estaria o risco de fugas ou bloqueios?

## Próximo passo

[classes.md](classes.md) ou volte ao [README.md](README.md).
