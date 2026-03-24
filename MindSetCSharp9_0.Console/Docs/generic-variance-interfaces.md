# Variança em interfaces genéricas — `out` e `in` (C# 4.0)

## Contexto

Em **C# 4.0**, interfaces (e certos delegados) genéricos podem declarar **parâmetros de tipo covariantes** com **`out`** ou **contravariantes** com **`in`**, quando as regras de segurança de tipos o permitem.

- **Covariância (`out T`)**: pode usar `IEnumerable<string>` onde se espera `IEnumerable<object>` — **só** “**sai**” `T` (ex.: elementos produzidos), não se aceita `T` como entrada que quebra a segurança.
- **Contravariância (`in T`)**: pode usar `IComparer<object>` onde se pede `IComparer<string>` — o tipo “**entra**” para comparação de instâncias mais derivadas.

Isto completou o quadro iniciado em C# 2.0 com **variança em delegados**; ver o enquadramento histórico em [covariance-contravariance.md](covariance-contravariance.md).

## O que praticar

1. Ler assinaturas BCL: `IEnumerable<out T>`, `IEnumerator<out T>`, `IComparable<in T>`, …
2. Porque **`List<T>`** não é covariante: `List<string>` **não** substitui `List<object>` — poderia permitir escrita insegura.
3. Declarar a sua própria interface `interface IProdutor<out T> { T Obter(); }` quando o desenho for só de **produção** de `T`.

## Exemplo mínimo

```csharp
IEnumerable<string> nomes = new[] { "a", "b" };
IEnumerable<object> objs = nomes; // covariância out T em IEnumerable<T>
```

## Mindset

Útil para **APIs genéricas** limpas; exige entender **por que** certas combinações `in`/`out` são rejeitadas pelo compilador.

## Próximo passo

[embedded-interop-types.md](embedded-interop-types.md)
