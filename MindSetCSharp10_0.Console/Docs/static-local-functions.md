# Funções locais `static` (C# 8.0)

## Ideia

Em **C# 8.0**, uma função local pode ser **`static`**: **não captura** variáveis do método encerrante (exceto `const`/`static` conforme regras), reduzindo **alocações** e **efeitos** implícitos.

## Exemplo

```csharp
int Sum(int[] xs)
{
    static int Add(int a, int b) => a + b;
    int t = 0;
    foreach (var x in xs) t = Add(t, x);
    return t;
}
```

## Mindset

- **Pureza** local quando não precisa de estado externo.

## Ver também

- [local-functions.md](local-functions.md) (C# 7.0)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
