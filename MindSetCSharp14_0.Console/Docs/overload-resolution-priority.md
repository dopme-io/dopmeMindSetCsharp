# Prioridade de resolução de overload (C# 13.0)

## Contexto

Autores de bibliotecas podem marcar uma sobrecarga como **preferida** em relação a outras com o atributo **`OverloadResolutionPriority`** — o compilador trata essa candidatura como **melhor** quando de outro modo seria ambíguo ou menos claro.

## O que praticar

Aplique o atributo a métodos sobrecarregados e observe a escolha do compilador em chamadas que antes escolhiam outra assinatura.

## Próximo passo

[csharp-12-0-overview.md](csharp-12-0-overview.md) · [csharp-13-0-overview.md](csharp-13-0-overview.md)
