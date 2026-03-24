# Argumentos nomeados não finais (C# 7.2)

## Ideia

Antes, se usasse **argumentos nomeados**, estes tinham de aparecer **à direita** de todos os posicionais (**à frente** na chamada). **C# 7.2** permite **misturar**: depois de um argumento **nomeado**, ainda pode seguir **outro argumento posicional** (desde que a posição corresponda ao parâmetro seguinte).

## Exemplo

```csharp
void M(int a, int b, int c) { }

M(1, b: 2, 3); // a=1, b=2, c=3
```

## Mindset

- Mais flexibilidade em chamadas geradas ou com **APIs** com muitos parâmetros opcionais.
- Chamadas muito **misturadas** podem **prejudicar** a leitura — prefira consistência na equipa.

## Ver também

- [named-optional-arguments.md](named-optional-arguments.md) (C# 4.0)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
