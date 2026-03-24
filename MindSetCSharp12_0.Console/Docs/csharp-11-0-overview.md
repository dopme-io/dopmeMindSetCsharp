# C# 11.0 — visão geral (novembro 2022)

## Contexto

**C# 11.0** acompanha **.NET 7** e continua a cadência anual. Os temas centrais: **matemática genérica** (algoritmos numéricos únicos para vários tipos), **ergonomia de strings** (raw literals, UTF-8 em compile-time, interpolação multilinha), **structs e inicialização** (`required`, default automático), **patterns** (list patterns, `Span<char>` vs literal), **tipos só visíveis no ficheiro** (`file`) para *source generators*, e extensões de **baixo nível** (`ref fields`, `scoped`, `nint`/`nuint` como aliases de `IntPtr`/`UIntPtr`).

O projeto **MindSetCSharp11_0.Console** define **`LangVersion` 11** no `.csproj` para limitar o conjunto de linguagem ao C# 11 (o SDK pode ser mais recente).

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| *Raw string literals* | [raw-string-literals.md](raw-string-literals.md) |
| Matemática genérica (`INumber<T>`, operadores estáticos em interfaces, …) | [generic-math.md](generic-math.md) |
| Atributos genéricos | [generic-attributes.md](generic-attributes.md) |
| Literais UTF-8 (`u8`) | [utf8-string-literals.md](utf8-string-literals.md) |
| Novas linhas em expressões de interpolação | [interpolated-newlines.md](interpolated-newlines.md) |
| *List patterns* | [list-patterns.md](list-patterns.md) |
| Tipos `file` (*file-local*) | [file-local-types.md](file-local-types.md) |
| Membros `required` | [required-members.md](required-members.md) |
| *Auto-default structs* | [auto-default-structs.md](auto-default-structs.md) |
| Pattern `ReadOnlySpan<char>` / `Span<char>` com literal constante | [pattern-span-char-constant-string.md](pattern-span-char-constant-string.md) |
| `nameof` alargado | [extended-nameof.md](extended-nameof.md) |
| `nint` / `nuint` como aliases de `IntPtr` / `UIntPtr` | [nint-nuint-inptr-aliases.md](nint-nuint-inptr-aliases.md) |
| `ref fields` e `scoped ref` | [ref-fields-scoped-ref.md](ref-fields-scoped-ref.md) |
| Conversão de *method group* para delegado (melhorada) | [method-group-delegate-improved.md](method-group-delegate-improved.md) |
| *Warning wave* 7 | [warning-wave-7.md](warning-wave-7.md) |

## Edições anteriores na mesma pasta

Guias **10.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[raw-string-literals.md](raw-string-literals.md) ou [list-patterns.md](list-patterns.md)
