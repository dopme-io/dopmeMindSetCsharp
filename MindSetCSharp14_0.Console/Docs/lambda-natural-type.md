# Tipo natural da expressão lambda (C# 10.0)

## Contexto

O compilador pode inferir um **tipo delegado** a partir da **lambda** ou **grupo de métodos** quando o alvo é claro — `var f = () => 1;` pode tipar `f` como `Func<int>` sem anotação explícita (conforme regras de inferência).

## Próximo passo

[lambda-explicit-return-type.md](lambda-explicit-return-type.md) · [csharp-10-0-overview.md](csharp-10-0-overview.md)
