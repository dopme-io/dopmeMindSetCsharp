# Interfaces (C# 1.0)

## Contexto

**Interfaces** definem um **contrato**: membros que quem implementa deve expor. Em C# 1.0, uma classe podia implementar **várias** interfaces; isso contornava a limitação de **herança simples** entre classes.

## O que implementar / praticar

1. Nomear interfaces com **substantivo** ou adjetivo acionável (`IDisposable`, `IComparable` — estilo .NET).
2. Manter interfaces **coesas**: poucos membros, mesma razão de mudança.
3. Implementação **explícita** (`void ILog.Escrever()`) quando quiser evitar poluir a API pública da classe.

## Exemplo mínimo

```csharp
public interface IFormatavel
{
    string ParaTexto();
}

public class Livro : IFormatavel
{
    private readonly string _titulo;

    public Livro(string titulo)
    {
        _titulo = titulo;
    }

    public string ParaTexto()
    {
        return "Livro: " + _titulo;
    }
}
```

## Mindset

- Interface = **capacidade** (“pode ser comparado”, “pode ser descartado”).
- Classe base = **relação é-um** forte com implementação partilhada.

## O que C# 1.0 *não* tinha

Interfaces **genéricas** (`IEnumerable<T>`) chegaram com genéricos em C# 2.0.

## Próximo passo

[events.md](events.md) — notificação com base em delegates, padrão observador na plataforma .NET.
