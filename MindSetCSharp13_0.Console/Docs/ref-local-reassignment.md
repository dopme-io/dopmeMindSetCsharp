# Reatribuir variáveis `ref` locais (C# 7.2)

## Ideia

Em **C# 7.0**, **`ref` locals** podiam referenciar um armazenamento, mas a **reatribuição** da variável `ref` a **outro** local era **proibida**. **C# 7.2** permite **rebind**: a variável `ref` pode passar a referenciar **outro** local (desde que tipos e regras de segurança o permitam).

## Exemplo ilustrativo

```csharp
void Example(ref int a, ref int b)
{
    ref int r = ref a;
    r = 1;
    r = ref b; // 7.2+: reatribuir para onde 'r' aponta
    r = 2;
}
```

## Mindset

- Útil em algoritmos que alternam entre **duas** localizações sem duplicar lógica.
- Aumenta a **complexidade** de leitura — use com moderação e nomes claros.

## Ver também

- [ref-locals-returns.md](ref-locals-returns.md) (C# 7.0)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
