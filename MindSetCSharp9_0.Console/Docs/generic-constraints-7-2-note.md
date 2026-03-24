# Restrições genéricas — nota (C# 7.2 vs 7.3)

## O que costuma confundir

Materiais que listam "mais restrições genéricas" perto de **C# 7.2** referem-se muitas vezes, no conjunto do ecossistema **2017–2018**, a:

- **`ref` / `in` / `readonly struct` / `ref struct`**, que **interagem** com métodos e tipos genéricos de formas novas (por exemplo, **passagem** e **retorno** por referência com segurança).
- A restrição **`where T : unmanaged`**, que é própria do **C# 7.3** (tipos **blittable** / sem referências de objeto em `T`).

## Recomendação MindSet

- Para **C# 7.2**, estude **[readonly-struct.md](readonly-struct.md)**, **[ref-struct.md](ref-struct.md)** e **[in-parameter-modifier.md](in-parameter-modifier.md)** como base para **genéricos** com structs e referências.
- Para **`unmanaged`**, veja uma futura edição MindSet **7.3** ou a documentação Microsoft de **C# 7.3**.

## Ver também

- [csharp-7-2-overview.md](csharp-7-2-overview.md)
