# Expressão condicional `ref` (`?:`) (C# 7.2)

## Ideia

O resultado de **`condição ? ref a : ref b`** pode ser **`ref`**: ambos os ramos devem ser **LValues** compatíveis e o resultado é uma **referência** ao ramo escolhido, não uma cópia do valor.

## Exemplo ilustrativo (unsafe de conceito)

```csharp
ref int Pick(bool flag, ref int x, ref int y)
{
    return ref (flag ? ref x : ref y);
}
```

## Mindset

- Evita **duplicar** atribuições `if/else` quando só muda **para onde** escrever.
- Erros de compilação aparecem se os ramos não forem referências válidas ou tipos incompatíveis.

## Ver também

- [ref-local-reassignment.md](ref-local-reassignment.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
