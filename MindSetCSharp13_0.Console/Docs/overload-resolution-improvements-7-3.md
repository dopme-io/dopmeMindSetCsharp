# Resolução de métodos e overloads (C# 7.3)

## Ideia

**C# 7.3** melhorou regras de **resolução de overload** em dois eixos frequentes na prática:

1. **Argumentos `in`** — escolha mais clara quando candidatos diferem por **`in`** vs **por valor**, alinhada à intenção de **evitar cópias** em structs grandes.
2. **Menos casos ambíguos** — o compilador aplica **regras** atualizadas para reduzir situações em que várias sobrecargas pareciam igualmente válidas sem um critério útil.

## Mindset

- Com **`in`**, **`readonly struct`**, e tipos grandes, a **assinatura correta** importa para performance **e** para desambiguação.
- Em caso de erro de compilação novo após atualizar SDK, consulte as **notas de breaking** / documentação Roslyn da versão.

## Ver também

- [in-parameter-modifier.md](in-parameter-modifier.md) (C# 7.2)
- [named-optional-arguments.md](named-optional-arguments.md) (C# 4.0)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
