# Eventos (C# 1.0)

## Contexto

**Eventos** são um mecanismo de **notificação**: um objeto publica que “algo aconteceu” e outros subscrevem reações. Em C# 1.0, eventos assentam em **delegates** com convenção `sender` + `EventArgs` (ou derivados).

## O que implementar / praticar

1. Declarar um delegate (ou reutilizar `EventHandler`) e um campo `event`.
2. **Disparar** o evento apenas a partir do dono do evento (encapsulamento típico).
3. Subscrever com **método nomeado** (C# 1.0 não tinha lambdas).

## Exemplo mínimo

```csharp
public class BotaoSimulado
{
    // Com nullable reference types ativado no SDK atual, use EventHandler? para evitar avisos.
    public event EventHandler? Clicado;

    public void SimularClique()
    {
        if (Clicado != null)
        {
            Clicado(this, EventArgs.Empty);
        }
    }
}

// Uso (C# 1.0 usaria método nomeado):
public static class DemoEventos
{
    public static void Executar()
    {
        var b = new BotaoSimulado();
        b.Clicado += AoClicar;
        b.SimularClique();
    }

    private static void AoClicar(object? sender, EventArgs e)
    {
        System.Console.WriteLine("Clicado.");
    }
}
```

Nota: em compiladores modernos, o padrão `?.Invoke` substitui o `if (Clicado != null)` de forma segura para threading; em estudo de C# 1.0, o `if` explícito reflete a época.

## Mindset

- Evento = **contrato de reação**: quem publica não conhece todos os consumidores.
- Evite lógica pesada nos handlers: risco de bloquear quem dispara o evento.

## Próximo passo

[properties.md](properties.md) — acesso controlado a estado sem expor campos diretamente.
