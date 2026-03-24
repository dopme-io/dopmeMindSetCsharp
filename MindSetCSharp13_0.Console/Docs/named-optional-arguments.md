# Argumentos nomeados e parâmetros opcionais (C# 4.0)

## Contexto

**Parâmetros opcionais** permitem **valores por defeito** na assinatura do método (como em C++ ou VB): quem chama pode omitir argumentos. **Argumentos nomeados** permitem indicar **`nome:`** na chamada, mudando a **ordem** ou saltando opcionais de forma legível.

Juntos, reduzem a necessidade de **muitas sobrecargas** que só diferem em combinações de parâmetros opcionais.

## O que praticar

1. `void Log(string msg, bool erro = false, int nivel = 0)`
2. Chamada: `Log("falhou", erro: true);` ou `Log(nivel: 2, msg: "ok");`
3. **Resolução**: os opcionais são compilados com atributos e valores por defeito na **caller** (atenção a **evolução de bibliotecas** e binários: mudar defeitos pode afetar quem já foi compilado).

## Exemplo mínimo

```csharp
static void Mover(int x, int y = 0, string etiqueta = "origem")
{
    System.Console.WriteLine(etiqueta + ": " + x + "," + y);
}

// Mover(10);
// Mover(10, etiqueta: "destino");
// Mover(y: 5, x: 1);
```

## Mindset

Clareza nas chamadas longas; cuidado com **demasiados** opcionais num único método — pode esconder complexidade.

## Próximo passo

[generic-variance-interfaces.md](generic-variance-interfaces.md)
