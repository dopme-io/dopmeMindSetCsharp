# Código seguro e desempenho — tema 7.3 (e continuidade 7.2)

## Ideia

A documentação de **C# 7.3** enfatiza que **código seguro** pode aproximar-se do desempenho de **unsafe** quando se combinam **structs**, **`ref`/`in`**, **`stackalloc`**, **`Span`**, e — em **7.3** — a restrição **`unmanaged`** para cenários de ponteiros controlados.

Vários mecanismos listados com esse tema apareceram ou foram refinados já em **7.2**:

| Tema | Guia (nesta pasta, herdado da edição 7.2) |
|------|---------------------------------------------|
| Campos `fixed` / menos *pinning* | [fixed-fields-without-pinning.md](fixed-fields-without-pinning.md) |
| Reatribuir `ref` locals | [ref-local-reassignment.md](ref-local-reassignment.md) |
| Inicializadores `stackalloc` | [stackalloc-initializers.md](stackalloc-initializers.md) |
| `fixed` com *pattern* (ex. Span) | [fixed-statements-pattern.md](fixed-statements-pattern.md) |

Em **7.3**, o destaque novo para **genéricos** é **`where T : unmanaged`** — ver [generic-constraint-unmanaged.md](generic-constraint-unmanaged.md).

## Ver também

- [csharp-7-3-overview.md](csharp-7-3-overview.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
