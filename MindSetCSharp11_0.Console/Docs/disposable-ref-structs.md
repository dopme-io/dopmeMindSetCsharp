# `ref struct` descartável (C# 8.0)

## Ideia

Um **`ref struct`** pode implementar **`IDisposable`** (e `using`/`await using` onde aplicável), permitindo **libertação** de recursos ligados a **janelas** de memória stack/Span.

## Mindset

- **RAII** para tipos de stack-only sem promover a heap.
- Regras de **lifetime** continuam estritas; consulte a documentação da sua versão do SDK.

## Ver também

- [ref-struct.md](ref-struct.md) (C# 7.2)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
