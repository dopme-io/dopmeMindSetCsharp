# Structs (C# 1.0)

## Contexto

**Structs** são **tipos valor**: em geral copiados por valor, alinhados a padrões numéricos e geometria simples. Em C# 1.0, `struct` já permitia campos, métodos, construtores (com regras específicas) e implementação de interfaces — mas **não** suportava herança de classe (apenas `System.ValueType` implicitamente).

## O que implementar / praticar

1. Usar `struct` quando o tipo for **pequeno**, **imutável** ou quase imutável, e copiar por valor for natural.
2. Evitar structs **mutáveis** grandes: cópias inadvertidas geram bugs difíceis.
3. Lembrar: `default(StructTipo)` zera campos; construtores devem inicializar **todos** os campos (regra histórica importante).

## Exemplo mínimo

```csharp
public struct Celsius
{
    private readonly double _valor;

    public Celsius(double valor)
    {
        _valor = valor;
    }

    public double Valor
    {
        get { return _valor; }
    }

    public override string ToString()
    {
        return _valor.ToString("0.0") + " °C";
    }
}
```

## Classes vs structs (mindset)

- **Classe**: identidade, ciclo de vida, referência partilhada.
- **Struct**: valor autocontido, semântica de “número” ou “medida”.

## O que evoluiu depois

`readonly struct`, `ref struct` e outras refinamentos são posteriores a 1.0; o documento foca a ideia base.

## Mindset — perguntas

- Faz sentido **duas variáveis** deste tipo terem o mesmo conteúdo e serem consideradas “iguais” sem partilhar o mesmo objeto na memória?
- O tamanho em memória é **pequeno** e estável?

## Próximo passo

[interfaces.md](interfaces.md) — contratos sem comprometer uma única árvore de herança.
