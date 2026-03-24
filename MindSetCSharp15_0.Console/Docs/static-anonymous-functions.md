# Funções anónimas `static` (C# 9.0)

## Contexto

Lambdas e métodos anónimos podem ser marcados com **`static`**: **não capturam** variáveis do estado encerrante (apenas `const`, `static`, etc., conforme regras), semelhante a [static-local-functions.md](static-local-functions.md) mas para **lambdas**.

## Exemplo

```csharp
int x = 1;
Func<int, int> f = static n => n + 1; // não usa x
```

## Próximo passo

[target-typed-conditional.md](target-typed-conditional.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
