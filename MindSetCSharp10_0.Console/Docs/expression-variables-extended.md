# Variáveis de expressão em mais localizações (C# 7.3)

## Ideia

**C# 7.3** alargou os sítios onde pode declarar **variáveis de expressão** (por exemplo **`out var`**, padrões com variáveis introduzidas) para cobrir **mais contextos** de expressão e instrução, reduzindo declarações antecipadas desnecessárias.

Os detalhes exatos dependem da versão do compilador; em geral inclui **mais ramos** de **`switch`**, inicializadores, e posições onde o compilador consegue provar o âmbito e o tipo.

## Mindset

- Continuação da linha **7.0+**: menos ruído, **âmbito** o mais restrito possível.
- Se o compilador recusar um sítio, verifique **LangVersion** e a documentação da sua versão do SDK.

## Ver também

- [out-variables.md](out-variables.md) (C# 7.0)
- [pattern-matching.md](pattern-matching.md) (C# 7.0)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
