# Inicializadores de módulo (C# 9.0)

## Contexto

Métodos estáticos anotados com **`[ModuleInitializer]`** são invocados pelo *runtime* quando o **assembly** é carregado — útil para **geradores de código** e inicialização única de módulo **sem** expor API pública.

## Exemplo

```csharp
internal static class Init
{
    [System.Runtime.CompilerServices.ModuleInitializer]
    internal static void Boot()
    {
        // executado uma vez no carregamento do assembly
    }
}
```

## Próximo passo

[partial-methods-csharp-9.md](partial-methods-csharp-9.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
