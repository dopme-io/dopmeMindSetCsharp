# Iteradores — yield (C# 2.0)

## Contexto

**Iteradores** permitem implementar **`IEnumerable`** / **`IEnumerator`** (e equivalentes genéricos) de forma **incremental**, usando **`yield return`** e **`yield break`**. O compilador gera uma máquina de estados.

Isto melhorou muito a **legibilidade** face a implementações manuais de `MoveNext`/`Current`.

## O que implementar / praticar

1. Método que devolve **`IEnumerable<T>`** com vários `yield return`.
2. Terminar cedo com **`yield break`**.
3. Compreender que a execução é **lazy** (só avança quando o consumidor pede o próximo elemento).

## Exemplo mínimo

```csharp
public static IEnumerable<int> PrimeirosN(int n)
{
    for (int i = 0; i < n; i++)
    {
        yield return i;
    }
}

// foreach (var x in PrimeirosN(5)) ...
```

## Relação com `foreach`

`foreach` consome o enumerador; com C# 1.2+, **`Dispose`** é chamado quando aplicável — combina bem com iteradores que implementam `IDisposable` no tipo gerado.

## Mindset

- Pensar em **sequência** e **passos**, não em índices manuais expostos.
- Cuidado com **efeitos laterais**: podem correr mais tarde do que espera devido à avaliação preguiçosa.

## Próximo passo

[covariance-contravariance.md](covariance-contravariance.md)
