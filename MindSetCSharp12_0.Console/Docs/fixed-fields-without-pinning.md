# Acesso a campos `fixed` sem *pinning* (C# 7.2)

## Ideia

**C# 7.2** permite **aceder** a **campos `fixed`** dentro de structs de forma mais **direta** em certos contextos, **sem** um `fixed` explícito adicional à volta do acesso, quando as regras do compilador garantem que o acesso é seguro (por exemplo, dentro de um **`fixed`** já ativo ou em padrões suportados).

Isto simplifica código que trabalha com **buffers embutidos** em structs (interop, performance).

## Mindset

- Menos cerimónia nos **hot paths** que manipulam memória fixa.
- A semântica **unsafe** não desaparece: continue a respeitar **alinhamento**, **tamanho** e **tempo de vida** dos buffers.

## Ver também

- [fixed-statements-pattern.md](fixed-statements-pattern.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
