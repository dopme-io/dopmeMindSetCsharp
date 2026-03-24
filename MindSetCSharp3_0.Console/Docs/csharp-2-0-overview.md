# C# 2.0 — visão geral (novembro 2005)

## Contexto

**C# 2.0** saiu com o **Visual Studio 2005** e o **.NET 2.0**. A linguagem deixou de ser só “OO clássica com `Object` por todo o lado”: **genéricos** permitiram que tipos e métodos operassem sobre um **parâmetro de tipo** mantendo **segurança de tipos em tempo de compilação**.

Em vez de `ArrayList` com boxing/casting ou de derivar `ListInt` de uma lista não genérica, passa a ser natural ter **`List<string>`**, **`List<int>`**, etc., e o compilador valida as operações.

## Iteradores

Os **iteradores** (`yield return` / `yield break`) tornaram-se parte da linguagem: é muito mais legível expor sequências consumíveis com **`foreach`** sem implementar manualmente `IEnumerator` em muitos cenários.

## O que este roteiro cobre

Os documentos em `Docs/` detalham cada área. Use **SDK .NET atual** para experimentar; as notas indicam o que é conceito **2.0** vs evoluções posteriores (ex.: variança genérica `in`/`out` em interfaces é **C# 4.0**).

## Mindset

- **Genéricos**: parametrizar o *tipo* sem perder verificação estática.
- **Iteradores**: descrever *como* produzir elementos; o compilador gera o enumerador.

## Próximo passo

[generics.md](generics.md)
