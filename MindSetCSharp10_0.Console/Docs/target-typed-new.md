# Expressões `new` com tipo alvo (C# 9.0)

## Contexto

Quando o **tipo** já é conhecido pelo contexto (lado esquerdo, `return`, argumento), pode usar **`new()`** sem repetir o nome do tipo — **target-typed `new`**.

## Exemplo

```csharp
System.Collections.Generic.List<int> xs = new() { 1, 2, 3 };
Point p = new(10, 20);
```

Reduz ruído quando o tipo já está declarado ou inferido.

## Próximo passo

[static-anonymous-functions.md](static-anonymous-functions.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
