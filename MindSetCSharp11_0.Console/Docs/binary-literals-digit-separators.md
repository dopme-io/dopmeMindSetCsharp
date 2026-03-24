# Literais binários e separadores de dígitos (C# 7.0)

## Contexto

- **Literais binários**: prefixo **`0b`** ou **`0B`**, por exemplo `0b1010` para dez.
- **Separadores de dígitos** **`_`** em literais numéricos: `1_000_000`, `0xFF_EC_DE_5E`, `0b1010_1100` — melhoram **legibilidade** sem alterar o valor.

## O que praticar

1. Máscaras de bits e enums com `0b…`.
2. Constantes financeiras ou de tempo `60_000` ms.
3. Posição dos `_`: não pode ser no início/fim nem adjacente a `0x`, `0b`, etc. (regras do compilador).

## Exemplo mínimo

```csharp
const int milhao = 1_000_000;
const int flags = 0b1010_1111;
```

## Mindset

Documentação **no próprio literal** — especialmente útil em código de **protocolos** e **bitmaps**.

## Próximo passo

[throw-expressions.md](throw-expressions.md)
