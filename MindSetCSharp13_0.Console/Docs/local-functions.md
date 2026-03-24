# Funções locais (C# 7.0)

## Contexto

**Funções locais** são métodos **aninhados** dentro de outro membro. Têm acesso ao âmbito lexicocal (variáveis locais da função “pai”) e são úteis para **extrair** lógica sem expor `private` na classe inteira — por exemplo validações repetidas num único método público.

Diferença conceptual de **lambda** atribuída a `delegate`: função local **não** é um objeto alocado por defeito da mesma forma; o compilador pode **inline** ou otimizar de modo diferente.

## O que praticar

1. `void Outer() { int Add(int a, int b) => a + b; … }`
2. Funções locais **recursivas** (ex.: parsing) com claridade frente a lambda recursiva.
3. `async` local functions (evoluções; em 7.0 já há cenários suportados — confirme na documentação da sua versão alvo).

## Exemplo mínimo

```csharp
static int SomarPares(int[] numeros)
{
    bool Par(int x) => x % 2 == 0;

    int total = 0;
    foreach (var n in numeros)
        if (Par(n)) total += n;
    return total;
}
```

## Mindset

**Encapsular** detalhe ao pé do uso, sem poluir a API da classe.

## Próximo passo

[expression-bodied-members-expanded.md](expression-bodied-members-expanded.md)
