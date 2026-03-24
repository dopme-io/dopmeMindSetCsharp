# Operadores `==` e `!=` em tipos tuplo (C# 7.3)

## Ideia

Em **C# 7.3**, tipos **tuplo** (`(T1, T2, …)`) suportam comparação de **igualdade** com **`==`** e **`!=`**: os comparadores compõem-se elemento a elemento com a semântica habitual de igualdade de cada membro.

## Exemplo

```csharp
var a = (1, "x");
var b = (1, "x");
bool same = a == b;
bool diff = a != (2, "x");
```

## Mindset

- Menos **`Equals`** explícito ou desconstrução só para comparar tuplos simples.
- Cuidado com **referências** e **nullability** nos membros — a semântica segue as regras de cada tipo.

## Ver também

- [tuples-deconstruction.md](tuples-deconstruction.md) (C# 7.0)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
