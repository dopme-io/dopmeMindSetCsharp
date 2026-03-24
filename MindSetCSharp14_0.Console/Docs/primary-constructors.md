# Construtores primários (C# 12.0)

## Contexto

**Construtores primários** permitem declarar parâmetros no **cabeçalho** da `class` ou `struct`; ficam disponíveis como **campos** no corpo do tipo (com regras de captura semelhantes às de *records* com parâmetros posicionais, aplicadas mais amplamente).

## O que praticar

```csharp
public class Service(ILogger log, string name)
{
    public void Run() => log.LogInformation("{Name}", name);
}
```

Compare com *records* em [records.md](records.md) (C# 9).

## Próximo passo

[collection-expressions.md](collection-expressions.md) · [csharp-12-0-overview.md](csharp-12-0-overview.md)
