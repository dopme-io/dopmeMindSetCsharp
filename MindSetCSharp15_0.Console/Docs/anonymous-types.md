# Tipos anónimos (C# 3.0)

## Contexto

**Tipos anónimos** geram **no compilador** uma classe imutável (efetivamente só `get` públicos) com propriedades definidas na expressão `new { … }`. São frequentes em **projeções LINQ** antes de mapear para um tipo nomeado.

## O que praticar

1. `var x = new { Nome = "Li", Idade = 30 };`
2. Usar em `select` em expressões de consulta (ver [query-expressions-linq.md](query-expressions-linq.md)).
3. Lembrar: o **nome** do tipo é gerado e **não** pode ser referenciado no código-fonte fora de `var` ou `object` (sem reflexão).

## Exemplo mínimo

```csharp
var resumo = new { Total = 42, Ok = true };
Console.WriteLine(resumo.Total);
```

## Mindset

Útil para **consultas ad hoc** e APIs internas; para **fronteiras** de módulo ou serialização estável, prefira tipos **nomeados**.

## Próximo passo

[lambda-expressions.md](lambda-expressions.md)
