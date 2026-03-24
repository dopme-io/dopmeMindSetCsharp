# `ref` locals e `ref` returns (C# 7.0)

## Contexto

**`ref` locals** permitem que uma variável local seja um **alias** para outro armazenamento (por exemplo um elemento de array ou um campo através de um `ref` return).

**`ref` returns** permitem que um método devolva **referência** a um local interno (ex.: slot num **buffer** pré-alocado), evitando cópia de structs grandes ou permitindo mutação direta do alvo.

Requer **cuidado**: APIs com `ref` expõem **aliases** e podem violar invariantes se o tempo de vida não for respeitado — o compilador impõe regras (ex.: não devolver `ref` a local que morre).

## O que praticar

1. `ref int r = ref arr[index]; r = 42;`
2. `ref readonly` (evoluções posteriores) para retornos só leitura — em 7.0 concentre-se em `ref` básico.
3. Quando **não** usar: a maioria do código de negócio segue feliz sem `ref`.

## Exemplo mínimo

```csharp
static ref int Encontrar(int[] items, int valor)
{
    for (int i = 0; i < items.Length; i++)
        if (items[i] == valor)
            return ref items[i];
    throw new System.InvalidOperationException("não encontrado");
}
```

## Mindset

**Performance** e **semântica de baixo nível** — para bibliotecas (`Span<T>` depois, etc.), não para cada propriedade de DTO.

## Próximo passo

[discards.md](discards.md)
