# Atributos em funções locais (C# 9.0)

## Contexto

Funções locais podem levar **atributos** (por exemplo `[Conditional]`, atributos de interoperabilidade ou análise), alinhando-as com métodos normais para **geradores** e **anotações**.

## Exemplo

```csharp
void Outer()
{
    [System.Diagnostics.Conditional("DEBUG")]
    static void LogLocal() { }

    LogLocal();
}
```

## Próximo passo

[csharp-9-0-overview.md](csharp-9-0-overview.md)
