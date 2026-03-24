# Membros com corpo de expressão — expansão (C# 7.0)

## Contexto

**C# 6.0** permitiu `=>` em métodos e propriedades simples. **C# 7.0** **estendeu** a construtores, **finalizadores** (`Finalize` em forma de `~Tipo()`), e **acessores** `get`/`set` de propriedades e indexadores — quando o corpo é uma **única expressão**.

Isto reduz ainda mais chavetas em membros triviais.

## O que praticar

1. Construtor: `public Ponto(int x, int y) => (X, Y) = (x, y);` com propriedades adequadas.
2. `public string Nome { get => campoNome; set => campoNome = value ?? ""; }`
3. Não forçar `=>` quando há **várias instruções** ou validação complexa.

## Exemplo mínimo

```csharp
public sealed class Rotulo
{
    private readonly string _texto;

    public Rotulo(string texto) => _texto = texto ?? "";

    public string Texto => _texto;
}
```

## Mindset

Continuação da **tersura** da 6.0 — legibilidade antes de “uma linha a todo o custo”.

## Próximo passo

[ref-locals-returns.md](ref-locals-returns.md)
