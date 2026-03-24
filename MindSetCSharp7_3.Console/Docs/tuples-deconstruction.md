# Tuplos e desconstrução (C# 7.0)

## Contexto

**C# 7.0** introduziu suporte de linguagem para **tuplos** com sintaxe leve `(T1, T2)` e **nomes de elemento** opcionais `(int id, string nome)`. Métodos podem devolver **vários valores** sem criar um tipo DTO dedicado para cada combinação.

A **desconstrução** permite `var (a, b) = tuplo` ou chamar um método `Deconstruct` em tipos personalizados.

> Os tuplos compilam em grande parte para **`System.ValueTuple`** (pacote / BCL conforme a framework).

## O que praticar

1. Retorno: `static (int Min, int Max) Limites(int[] xs) => (xs.Min(), xs.Max());`
2. Desconstrução: `var (menor, maior) = Limites(arr);`
3. **Discards** com tuplos: `var (x, _, z) = triplo;` — ver [discards.md](discards.md)

## Exemplo mínimo

```csharp
static (int Soma, int Produto) Acumular(int a, int b)
{
    return (a + b, a * b);
}

// var (s, p) = Acumular(3, 4);
```

## Mindset

Bom para **APIs internas** e algoritmos; para **contratos públicos** estáveis, avalie se um **tipo nomeado** não comunica melhor a intenção.

## Próximo passo

[pattern-matching.md](pattern-matching.md)
