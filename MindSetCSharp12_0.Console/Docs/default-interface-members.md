# Membros predefinidos de interface (C# 8.0)

## Ideia

Interfaces podem declarar **implementações predefinidas** de métodos e propriedades (e membros estáticos em evoluções). Isto permite **estender** contratos sem quebrar implementações existentes — novos membros podem ter corpo na interface.

**Requisito de runtime:** a **CLR** em **.NET Core 3.0+** foi estendida para suportar estes membros (não é só sintaxe do compilador).

## Exemplo

```csharp
interface ILogger
{
    void Log(string message);

    void LogError(string message) => Log($"ERROR: {message}");
}
```

## Mindset

- **Evolução** de APIs de interface com menos “helper” estático em paralelo.
- **Resolução de conflitos** e herança múltipla de interfaces: siga as regras da linguagem e testes.

## Ver também

- [interfaces.md](interfaces.md)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
