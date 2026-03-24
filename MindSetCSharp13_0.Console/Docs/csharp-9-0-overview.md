# C# 9.0 — visão geral (novembro 2020)

## Contexto

**C# 9.0** saiu com **.NET 5**. É a **versão predefinida da linguagem** para assemblies que visam **.NET 5**. O desenho continua três linhas das edições anteriores: **menos cerimónia**, **separar dados de algoritmos** e **mais padrões em mais sítios**.

- **Top-level statements**: o programa principal pode existir **sem** `namespace`, classe `Program` e `static void Main()` — leitura mais directa.
- **Records**: sintaxe concisa para tipos referência com **semântica de igualdade por valor**; contentores de dados com comportamento mínimo. **`init`** e expressões `with` suportam **mutação não destrutiva**.
- **Retornos covariantes**: tipos derivados podem substituir métodos virtuais devolvendo um tipo **mais derivado** que o da base (incl. em hierarquias de records).

## Funcionalidades (índice)

| Tema | Ficheiro |
|------|----------|
| *Records* | [records.md](records.md) |
| *Setters* só `init` | [init-only-setters.md](init-only-setters.md) |
| Instruções de nível superior | [top-level-statements.md](top-level-statements.md) |
| Patterns relacionais e lógicos (`<`, `>`, `and`, `or`, `not`, …) | [pattern-relational-logical.md](pattern-relational-logical.md) |
| Inteiros de tamanho nativo (`nint` / `nuint`) | [native-sized-integers.md](native-sized-integers.md) |
| Ponteiros de função | [function-pointers.md](function-pointers.md) |
| Omitir `localsinit` (desempenho / interop) | [skip-localsinit.md](skip-localsinit.md) |
| Inicializadores de módulo | [module-initializers.md](module-initializers.md) |
| Métodos parciais (novas regras) | [partial-methods-csharp-9.md](partial-methods-csharp-9.md) |
| `new` com tipo alvo | [target-typed-new.md](target-typed-new.md) |
| Funções anónimas `static` | [static-anonymous-functions.md](static-anonymous-functions.md) |
| Expressão condicional com tipo alvo | [target-typed-conditional.md](target-typed-conditional.md) |
| Tipos de retorno covariantes | [covariant-return-types.md](covariant-return-types.md) |
| `GetEnumerator` de extensão e `foreach` | [extension-getenumerator-foreach.md](extension-getenumerator-foreach.md) |
| Parâmetros de descarte em lambdas | [lambda-discard-parameters.md](lambda-discard-parameters.md) |
| Atributos em funções locais | [attributes-local-functions.md](attributes-local-functions.md) |

## Edições anteriores na mesma pasta

Guias **8.0** e anteriores estão em cópia local — ver [README.md](README.md).

## Próximo passo

[records.md](records.md) ou [top-level-statements.md](top-level-statements.md)

## Continuar para C# 10.0 (nesta pasta)

[csharp-10-0-overview.md](csharp-10-0-overview.md) — *record structs*, `global using`, *handlers* de interpolação, …
