# Descartes — `_` (C# 7.0)

## Contexto

O **discard** é a variável **descartável** escrita como **`_`**: indica “**não preciso deste valor**”. Útil com tuplos, `out`, pattern matching e **deconstrução** onde só interessa parte dos resultados.

## O que praticar

1. Tuplo: `var (nome, _, idade) = pessoa;` se o elemento do meio não importa.
2. `if (dict.TryGetValue(key, out _))` — só quer saber se existia.
3. `switch` / `is` com padrões onde alguns ramos usam `_` (conforme sintaxe suportada na versão).

## Exemplo mínimo

```csharp
static void IgnorarSegundo((int, int, int) triplo)
{
    var (a, _, c) = triplo;
    System.Console.WriteLine(a + c);
}
```

## Mindset

Comunica intenção **melhor** que variáveis `unused1` ou comentários.

## Próximo passo

[binary-literals-digit-separators.md](binary-literals-digit-separators.md)
