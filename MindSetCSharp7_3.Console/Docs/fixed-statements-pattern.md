# `fixed` com tipos que suportam um *pattern* (C# 7.2)

## Ideia

O **`fixed`** deixou de estar limitado a cenários muito específicos: tipos que oferecem o **padrão** adequado (por exemplo, **`GetPinnableReference()`** em tipos como **`Span<T>`** / **`ReadOnlySpan<T>`**) podem ser usados em **`fixed`**, permitindo obter um **ponteiro** onde a linguagem e o compilador garantem consistência.

## Mindset

- Ponte entre código **gerido** e **unsafe** de forma mais **estruturada** e alinhada com **Spans**.
- Continua a ser **`unsafe`** onde aplicável — mantenha o bloco `fixed` **curto** e documente invariantes.

## Ver também

- [fixed-fields-without-pinning.md](fixed-fields-without-pinning.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
