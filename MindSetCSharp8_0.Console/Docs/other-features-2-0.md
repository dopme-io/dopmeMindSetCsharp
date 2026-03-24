# Outras capacidades C# 2.0 (extensões ao que já existia)

## Contexto

Além dos tópicos principais, C# 2.0 **reforçou** funcionalidades existentes.

### Acessibilidade separada em get / set

Propriedades podem ter **`public get`** e **`private set`** (ou outras combinações), reforçando encapsulamento sem métodos auxiliares verbosos.

```csharp
public class Contador
{
    private int _valor;

    public int Valor
    {
        get { return _valor; }
        private set { _valor = value; }
    }

    public void Incrementar()
    {
        Valor = Valor + 1;
    }
}
```

### Conversões de grupo de métodos → delegate

Pode atribuir **`NomeDoMetodo`** diretamente a uma variável delegate quando a assinatura coincide — **sem** `new DelegateType(Method)` explícito em muitos casos.

```csharp
Action<string> log = Console.WriteLine;
```

### Classes estáticas

**`static class`** — só membros estáticos; não instanciável; selada implicitamente.

```csharp
public static class MatematicaBasica
{
    public static int Dobro(int x)
    {
        return x * 2;
    }
}
```

### Inferência com delegados

Em conjunto com métodos anónimos e conversões de grupo de métodos, o compilador infere tipos em mais contextos, reduzindo ruído.

## Mindset

- **get/set** distintos: expor leitura pública e restringir escrita.
- **`static class`**: utilitários sem estado; não use como substituto de injeção de dependências moderna.

## Conclusão do bloco C# 2.0

Volte ao [README.md](README.md) ou aprofunde a base em [classes.md](classes.md) e restantes ficheiros da mesma pasta.
