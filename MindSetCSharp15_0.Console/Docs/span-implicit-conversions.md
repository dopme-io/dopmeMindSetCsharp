# Conversões implícitas para `Span<T>` / `ReadOnlySpan<T>` (C# 14.0)

## Contexto

O conjunto de **conversões implícitas** para **`Span<T>`** e **`ReadOnlySpan<T>`** foi alargado — por exemplo a partir de tipos de *buffer* ou literais suportados — reduzindo *casts* e alocações em código quente.

## O que praticar

Compare atribuições a `ReadOnlySpan<char>` a partir de literais e arrays entre C# 13 e 14.

## Próximo passo

[lambda-parameter-modifiers.md](lambda-parameter-modifiers.md) · [utf8-string-literals.md](utf8-string-literals.md) (C# 11) · [csharp-14-0-overview.md](csharp-14-0-overview.md)
