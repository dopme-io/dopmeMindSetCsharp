# Métodos parciais — novas regras (C# 9.0)

## Contexto

Em **C# 9**, métodos parciais podem ter **modificadores de acessibilidade** explícitos e **tipo de retorno não void**. Nesses casos, a **implementação** deixa de ser opcional: **tem** de existir uma definição.

Isto alinha métodos parciais com cenários de **geração de código** mais ricos (antes, muitos eram `private void` implícitos e opcionais).

## Ver também

[partial-methods.md](partial-methods.md) (visão histórica C# 3.0) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
