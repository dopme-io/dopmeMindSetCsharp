# Propriedades (C# 1.0)

## Contexto

**Propriedades** unem a sintaxe de acesso a **campos** com a disciplina de **métodos** `get`/`set`. Em C# 1.0 já existiam; o compilador gera métodos especiais (`get_X` / `set_X` na IL), úteis para depuração e COM interop.

## O que implementar / praticar

1. **Substituir campos públicos** por propriedades quando houver validação ou cálculo.
2. `get` público + `set` privado (ou protegido) para **só leitura externa** com escrita interna — em C# 1.0 escrevia-se o `set` com acessibilidade mais restrita quando necessário.
3. Propriedades **só leitura** com `get` e valor definido no construtor (sem `readonly` automático em propriedades — `readonly` era para campos).

## Exemplo mínimo (estilo C# 1.0)

```csharp
public class Retangulo
{
    private int _largura;
    private int _altura;

    public int Largura
    {
        get { return _largura; }
        set
        {
            if (value <= 0) throw new ArgumentOutOfRangeException(nameof(value));
            _largura = value;
        }
    }

    public int Altura
    {
        get { return _altura; }
        set
        {
            if (value <= 0) throw new ArgumentOutOfRangeException(nameof(value));
            _altura = value;
        }
    }

    public int Area
    {
        get { return _largura * _altura; }
    }
}
```

## Mindset

- Campo = detalhe de implementação; propriedade = **contrato de acesso** estável.
- Validação no `set` evita estado inválido **na fronteira**.

## O que veio depois

*Auto-properties*, *expression-bodied* members e `init` são evoluções posteriores.

## Próximo passo

[delegates.md](delegates.md) — referências tipadas a métodos, base de eventos e callbacks.
