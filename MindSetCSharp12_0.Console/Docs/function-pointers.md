# Ponteiros de função (C# 9.0)

## Contexto

**Function pointers** (`delegate*`) oferecem chamadas estilo delegado com **menos alocações** que instanciar um `Delegate` — relevante para **interop** nativo e hot paths.

## Exemplo (unsafe)

```csharp
unsafe
{
    static int Add(int a, int b) => a + b;
    delegate*<int, int, int> add = &Add;
    int s = add(2, 3);
}
```

Requer contexto **`unsafe`** e conformidade com as regras do compilador / plataforma.

## Próximo passo

[skip-localsinit.md](skip-localsinit.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
