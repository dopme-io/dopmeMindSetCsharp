# C# 13.0 — visão geral (novembro 2024)

## Contexto

**C# 13.0** acompanha **.NET 9** e alarga `params`, concorrência com **`System.Threading.Lock`**, literais e resolução de overload, `ref struct` e genéricos, membros **parciais** alargados, e **prioridade de overload** para autores de bibliotecas.

O projeto **MindSetCSharp13_0.Console** define **`LangVersion` 13** no `.csproj`.

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| `params` em coleções (`Span<T>`, interfaces, …) | [params-collections.md](params-collections.md) |
| `lock` com `System.Threading.Lock` (`EnterScope`, `ref struct`) | [lock-system-threading-lock.md](lock-system-threading-lock.md) |
| Escape `\e` (U+001B) | [escape-sequence-e.md](escape-sequence-e.md) |
| Resolução de overload e *method groups* (ajustes) | [overload-resolution-method-groups-csharp-13.md](overload-resolution-method-groups-csharp-13.md) |
| Índice `^` implícito em inicializadores de objeto | [implicit-index-from-end-object-initializers.md](implicit-index-from-end-object-initializers.md) |
| `ref` locals / `unsafe` em iteradores e `async` | [ref-locals-iterators-async.md](ref-locals-iterators-async.md) |
| `ref struct` que implementa interfaces | [ref-struct-implements-interface.md](ref-struct-implements-interface.md) |
| `ref struct` como argumento de tipo genérico | [ref-struct-type-arguments.md](ref-struct-type-arguments.md) |
| Propriedades e indexadores parciais | [partial-properties-indexers.md](partial-properties-indexers.md) |
| Prioridade de resolução de overload | [overload-resolution-priority.md](overload-resolution-priority.md) |

## Edições anteriores na mesma pasta

Guias **12.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[params-collections.md](params-collections.md) ou [lock-system-threading-lock.md](lock-system-threading-lock.md)
