# Argumentos em expressões de coleção (`with(...)`) (C# 15.0)

## Contexto

Em **expressões de coleção**, pode passar-se argumentos ao **construtor** ou **método de fábrica** da coleção de destino. O primeiro elemento da expressão é **`with(...)`**, seguido dos elementos (e opcionalmente *spread* `..`).

Isto permite definir **capacidade**, **comparers** ou outros parâmetros **dentro da mesma sintaxe** `[ … ]`.

## O que praticar

```csharp
string[] values = ["one", "two", "three"];

// Capacidade no construtor de List<T>
List<string> names = [with(capacity: values.Length * 2), .. values];

// Comparer no construtor de HashSet<T>
HashSet<string> set = [with(StringComparer.OrdinalIgnoreCase), "Hello", "HELLO", "hello"];
// Um único elemento: as três strings são iguais com OrdinalIgnoreCase
```

## Inicializadores de coleção

Para usar **argumentos** em **inicializadores de coleção** clássicos (sintaxe antiga), ver a documentação sobre **Object and Collection Initializers**.

## Próximo passo

[collection-expressions.md](collection-expressions.md) (C# 12) · [object-collection-initializers.md](object-collection-initializers.md) (C# 3) · [csharp-15-0-overview.md](csharp-15-0-overview.md)
