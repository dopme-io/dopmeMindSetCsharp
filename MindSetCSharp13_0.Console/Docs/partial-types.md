# Tipos parciais — partial types (C# 2.0)

## Contexto

**`partial class`**, **`partial struct`** e **`partial interface`** permitem dividir a definição de um tipo por **vários ficheiros**. O compilador funde as partes num único tipo. Útil para **designers** (WinForms gerava UI num ficheiro, lógica noutro) e para **código gerado** + código manual.

## O que implementar / praticar

1. Dividir uma classe em dois ficheiros `.cs` com a mesma assinatura `partial class Nome`.
2. Membros `partial void` (C# 3.0+) são posteriores; em 2.0 foque em **métodos e campos** repartidos.

## Exemplo mínimo

```csharp
// Ficheiro A
namespace Demo;

public partial class Servico
{
    public void Executar()
    {
        LogInterno("início");
    }
}

// Ficheiro B
namespace Demo;

public partial class Servico
{
    private void LogInterno(string msg)
    {
        System.Console.WriteLine("[Servico] " + msg);
    }
}
```

## Mindset

- **Coesão**: cada ficheiro com uma responsabilidade (ex.: persistência vs regras).
- Não abuse: demasiados `partial` espalhados dificultam leitura.

## Próximo passo

[anonymous-methods.md](anonymous-methods.md)
