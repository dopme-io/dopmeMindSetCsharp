# Classes (C# 1.0)

## Contexto

Em C# 1.0, **classes** são o principal mecanismo de **tipo referência** para modelar entidades com comportamento e estado. Herança simples (`class Derivada : Base`), membros `public`/`private`/`protected`/`internal`, construtores e destruidor (finalizador) já faziam parte do desenho.

## O que implementar / praticar

1. **Definir uma classe** com um nome em singular que represente um conceito estável (ex.: `Conta`, `Pedido`).
2. **Campos** para estado interno; **métodos** para operações que preservam invariantes (regras que sempre devem ser verdadeiras).
3. **Construtor** para garantir que o objeto nasce em estado válido.
4. **Encapsular**: exponha só o mínimo (`private` por defeito, `public` quando necessário).

## Exemplo mínimo

```csharp
public class Ponto
{
    private int _x;
    private int _y;

    public Ponto(int x, int y)
    {
        _x = x;
        _y = y;
    }

    public void Mover(int deltaX, int deltaY)
    {
        _x += deltaX;
        _y += deltaY;
    }

    public string Descrever()
    {
        return $"({_x}, {_y})";
    }
}
```

## O que C# 1.0 *não* tinha

- **Propriedades** existiam (ver [properties.md](properties.md)); não havia *auto-properties* (`public int X { get; set; }` só apareceu muito mais tarde).
- **Genéricos** (`List<T>`): em 1.0 usava-se `ArrayList`, `Hashtable`, etc., com *boxing* e menos segurança de tipos.

## Mindset — perguntas

- Esta classe representa **uma** responsabilidade clara?
- O estado pode ficar **inválido** se alguém esquecer de chamar um método? Como reduzir esse risco com o que C# 1.0 oferece?

## Próximo passo

[structs.md](structs.md) — tipos valor compactos, úteis quando a semântica é “valor”, não “identidade”.
