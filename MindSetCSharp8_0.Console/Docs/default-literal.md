# Literal `default` com tipo inferido (C# 7.1)

## Ideia

Antes, **`default(T)`** exigia o **tipo `T` explícito**. Em **C# 7.1**, pode usar-se o literal **`default`** sozinho quando o **tipo de destino** é conhecido pelo compilador (**target-typed default**).

## Exemplos

```csharp
void M(int x = default) { }

int n = default;
int? q = default;
var numbers = new int[] { default, 1, 2 }; // elementos int

// Com genéricos: o T resolve o significado de default
T CreateDefault<T>() => default;
```

## Mindset

- Reduz ruído onde o tipo já está fixado pelo **contexto** (parâmetro opcional, lado esquerdo de atribuição, elemento de array tipado, valor de retorno inferido).
- Não confundir com **`default`** em **`switch`** / patterns — aqui falamos só do **valor por omissão** do tipo.

## Ver também

- [csharp-7-1-overview.md](csharp-7-1-overview.md)
