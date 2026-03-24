# `_` à esquerda em literais numéricos (C# 7.2)

## Ideia

**C# 7.0** introduziu **separadores de dígitos** com **`_`** *entre* dígitos. **C# 7.2** permite **`_`** também **antes** do primeiro dígito significativo (por exemplo, após `0x` ou no início de grupos), alinhando com estilos de formatação em bases não decimais.

## Exemplo

```csharp
int hex = 0x_FF_FF;
int dec = 1_000;
```

(As regras exactas de posição válida de `_` dependem da base e da versão; o compilador avisa se for inválido.)

## Mindset

- Legibilidade em **máscaras**, **hex** e constantes **bit a bit**.

## Ver também

- [binary-literals-digit-separators.md](binary-literals-digit-separators.md) (C# 7.0)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
