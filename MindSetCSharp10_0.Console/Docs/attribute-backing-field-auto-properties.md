# Atributos no *backing field* de propriedades autoimplementadas (C# 7.3)

## Ideia

Para **propriedades autoimplementadas** (`{ get; set; }`), **C# 7.3** permite aplicar **atributos** ao **campo gerado pelo compilador** (o *backing field*) com o destino **`field:`**:

```csharp
public class C
{
    [field: NonSerialized]
    public int Id { get; set; }
}
```

Isto é útil para serialização, diagnóstico ou metadados que devem **afetar o armazenamento** e não só a superfície da propriedade.

## Mindset

- **Metadados** alinhados ao **estado** real quando o runtime ou ferramentas leem o campo.
- Prefira **APIs públicas** documentadas; atributos em campos gerados podem ser **frágeis** a mudanças do compilador se mal usados.

## Ver também

- [auto-implemented-properties.md](auto-implemented-properties.md) (C# 3.0)
- [attributes.md](attributes.md)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
