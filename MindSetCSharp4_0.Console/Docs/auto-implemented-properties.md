# Propriedades autoimplementadas (C# 3.0)

## Contexto

Antes de C# 3.0, uma propriedade simples exigia **campo de apoio** explícito e `get`/`set` manuais. Com **propriedades autoimplementadas**, o compilador gera o campo oculto.

## O que praticar

1. `public string Nome { get; set; }`
2. Restringir escrita: `public int Id { get; private set; }` (útil em construtores ou fábricas).
3. Comparar mentalmente com o padrão C# 2.0 em [other-features-2-0.md](other-features-2-0.md) (get/set com corpo explícito).

## Exemplo mínimo

```csharp
public sealed class Pessoa
{
    public string Nome { get; set; }
    public int Idade { get; set; }
}
```

> Em C# 3.0, sem **inicializadores de propriedade automática** (isso é **C# 6+**): use construtor ou aceite `null` / valor por defeito do tipo conforme o modelo.

## Mindset

Menos ruído para **DTOs** e modelos simples; quando há **lógica** em get/set, volte ao padrão com campo privado.

## Próximo passo

[object-collection-initializers.md](object-collection-initializers.md)
