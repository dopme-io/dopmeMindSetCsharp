# Expressões de consulta e LINQ (C# 3.0)

## Contexto

O **LINQ** (*Language-Integrated Query*) integra consultas declarativas na linguagem. Há duas faces:

- **Sintaxe de consulta**: `from x in xs where … select …`
- **Sintaxe de métodos**: `xs.Where(…).Select(…)` — em geral **equivalente** por *desugaring* do compilador.

Combinado com **métodos de extensão** e **genéricos** (C# 2.0), coleções tornam-se “mais inteligentes”: filtros, projeções, agregações (`Average`, `Sum`, …) sem laços manuais explícitos.

## O que praticar

1. `from n in numeros where n > 0 select n * 2`
2. A mesma expressão com `numeros.Where(n => n > 0).Select(n => n * 2)`
3. `using System.Linq;` e um tipo enumerável (`int[]`, `List<int>`, …)

## Exemplo mínimo

```csharp
using System.Linq;

var notas = new List<double> { 12.5, 14, 9, 15 };
var media = notas.Average();

var aprovados = from n in notas
                where n >= 10
                select n;
```

## Mindset

**Declarativo** sobre dados em memória (LINQ to Objects); outros provedores (EF, XML, …) partilham o *padrão* mental, com semânticas diferentes de execução.

## Próximo passo

[expression-trees.md](expression-trees.md)
