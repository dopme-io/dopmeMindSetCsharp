# Modificador `in` em parâmetros (C# 7.2)

## Ideia

**`in T x`** passa o argumento **por referência** (como **`ref`**), mas o **callee** compromete-se a **não modificar** `x`. Para **structs** grandes, evita **cópias** sem dar permissão de escrita.

## Exemplo

```csharp
static int Sum(in BigStruct a)
{
    return a.Field1 + a.Field2;
}
```

## Mindset

- **Performance** com **imutabilidade** aparente no contrato do método.
- Combine com **`readonly struct`** quando o tipo for conceptualmente imutável.

## Ver também

- [readonly-struct.md](readonly-struct.md)
- [ref-readonly-returns.md](ref-readonly-returns.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
