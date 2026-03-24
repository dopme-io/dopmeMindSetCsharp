# C# 7.2 — visão geral (novembro 2017)

## Contexto

**C# 7.2** é uma versão **incremental** focada em **segurança de memória**, **structs** (`readonly`, `ref`), **APIs de baixo nível** (`stackalloc`, `fixed`), e **ergonomia** (argumentos nomeados, literais numéricos, novo modificador de acesso).

A linguagem continuava a acompanhar **.NET Core 2.x** e **`Span<T>`** / tipos **`ref struct`**, com o compilador a alinhar regras de **referência** e **imutabilidade** ao que as APIs modernas exigiam.

## Funcionalidades (por tema)

| Tema | Ficheiro |
|------|----------|
| Inicializadores em `stackalloc` | [stackalloc-initializers.md](stackalloc-initializers.md) |
| `fixed` com tipos que seguem um *pattern* | [fixed-statements-pattern.md](fixed-statements-pattern.md) |
| Campos `fixed` sem *pinning* explícito extra | [fixed-fields-without-pinning.md](fixed-fields-without-pinning.md) |
| Reatribuir variáveis `ref` locais | [ref-local-reassignment.md](ref-local-reassignment.md) |
| `readonly struct` | [readonly-struct.md](readonly-struct.md) |
| Parâmetros `in` | [in-parameter-modifier.md](in-parameter-modifier.md) |
| Retornos `ref readonly` | [ref-readonly-returns.md](ref-readonly-returns.md) |
| `ref struct` | [ref-struct.md](ref-struct.md) |
| Restrições genéricas (nota 7.2 / 7.3) | [generic-constraints-7-2-note.md](generic-constraints-7-2-note.md) |
| Argumentos nomeados não finais | [non-trailing-named-arguments.md](non-trailing-named-arguments.md) |
| `_` à esquerda em literais numéricos | [leading-underscores-numeric-literals.md](leading-underscores-numeric-literals.md) |
| `private protected` | [private-protected-access.md](private-protected-access.md) |
| Expressão condicional `ref` (`?:`) | [conditional-ref-expressions.md](conditional-ref-expressions.md) |

## Edições anteriores na mesma pasta

Guias **7.1**, **7.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[readonly-struct.md](readonly-struct.md) ou [stackalloc-initializers.md](stackalloc-initializers.md)
