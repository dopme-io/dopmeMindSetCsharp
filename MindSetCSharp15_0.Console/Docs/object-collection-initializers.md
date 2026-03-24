# Inicializadores de objeto e de coleção (C# 3.0)

## Contexto

**Inicializadores de objeto** permitem definir propriedades (e campos acessíveis) **após** `new Tipo { … }` sem chamar um construtor longo para cada combinação. **Inicializadores de coleção** permitem `new List<int> { 1, 2, 3 }` em vez de vários `Add`.

## O que praticar

1. Objeto: `new Cliente { Nome = "Ana", Ativo = true }`.
2. Coleção: `new List<string> { "a", "b" }`.
3. Aninhamento: lista de objetos com inicializadores internos.

## Exemplo mínimo

```csharp
var pontos = new List<Ponto>
{
    new Ponto { X = 0, Y = 0 },
    new Ponto { X = 10, Y = 20 }
};

public sealed class Ponto
{
    public int X { get; set; }
    public int Y { get; set; }
}
```

## Mindset

Menos construtores “só para testes”; dados de configuração e testes ficam mais claros na **forma literal**.

## Próximo passo

[anonymous-types.md](anonymous-types.md)
