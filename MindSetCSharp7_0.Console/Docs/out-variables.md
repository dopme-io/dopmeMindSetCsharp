# Variáveis `out` inline (C# 7.0)

## Contexto

Antes do C# 7, era preciso **declarar** a variável `out` numa linha anterior à chamada. Em **C# 7.0**, pode escrever-se **`out var n`** ou **`out T n`** **dentro** da lista de argumentos: o compilador infere ou usa o tipo explícito e o âmbito da variável é o **bloco** envolvente.

## O que praticar

1. `if (int.TryParse(texto, out var n)) { … usar n … }`
2. `Dictionary.TryGetValue` com `out var valor`.
3. Comparar legibilidade com o padrão antigo (variável declarada antes).

## Exemplo mínimo

```csharp
static bool TentarDobro(string s, out int resultado)
{
    if (int.TryParse(s, out var x))
    {
        resultado = x * 2;
        return true;
    }
    resultado = 0;
    return false;
}
```

## Mindset

Menos **ruído** em torno de APIs com `out` — alinhado ao objetivo de código mais **limpo**.

## Próximo passo

[tuples-deconstruction.md](tuples-deconstruction.md)
