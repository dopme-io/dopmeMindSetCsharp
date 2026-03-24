# Covariância e contravariância (C# 2.0 — delegados e legado)

> **C# 4.0:** variança em **interfaces** genéricas (`out` / `in`, ex.: `IEnumerable<out T>`) — [generic-variance-interfaces.md](generic-variance-interfaces.md).

## Contexto

Em **C# 2.0**, a conversão **genérica** de interfaces com **`out` / `in`** (**variança em interfaces genéricas**) **ainda não existia** — isso chegou em **C# 4.0** (`IEnumerable<out T>`, etc.).

O que **2.0** trouxe de relevante nesta área, junto com **conversões de grupo de métodos**, é sobretudo:

1. **Delegados genéricos** e regras de atribuição entre tipos de delegate compatíveis (covariância de **tipo de retorno**, contravariância de **parâmetros** em cenários de delegate).
2. **Arrays** já eram **covariantes** desde C# 1.x (`string[]` como `object[]`) — útil de conhecer, mas com **armadilhas** em runtime se escrever num array com tipo elemento mais derivado.

## O que estudar em C# 2.0

1. Atribuir um **grupo de métodos** a um **`Func<...>`** / delegate personalizado quando assinaturas são compatíveis (retorno mais derivado / parâmetros mais base, conforme regras).
2. Ler a documentação histórica de **`Func`/`Action`** — em 2.0 usava-se muito **`Predicate<T>`**, **`Action<T>`**, **`Func<T,TResult>`** com **.NET 2.0**.

## Nota importante

Se vir **`IEnumerable<out T>`**, isso é **C# 4.0+**. Em 2.0, **`IEnumerable<T>`** existia mas **sem** variança anotada na interface.

## Exemplo ilustrativo (delegado)

```csharp
public delegate object Fabricador();

public static string CriarTexto() => "olá";

// Em cenários compatíveis, método que devolve string pode alimentar delegate que espera object (covariância de retorno em delegates).
Fabricador f = CriarTexto;
object o = f();
```

## Mindset

- **Covariância**: “posso usar onde esperam um tipo **mais geral**?”
- **Contravariância**: “posso passar algo que aceita **mais geral** onde pedem **mais específico**?”
- Sempre que possível, prefira **genéricos** a **arrays covariantes** para novos desenhos.

## Próximo passo

[other-features-2-0.md](other-features-2-0.md)
