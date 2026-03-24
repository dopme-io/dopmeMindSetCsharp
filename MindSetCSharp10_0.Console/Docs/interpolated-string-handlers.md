# *Handlers* de strings interpoladas (C# 10.0)

## Contexto

Em vez de sempre alocar `string`, uma **interpolated string** pode usar um **tipo handler** personalizado (`[InterpolatedStringHandler]`) que constrói o resultado por **append** — útil para **buffers**, **UTF8**, **logging** sem `string` intermédia.

O **.NET 6** aplica isto no runtime para **desempenho**.

## Mindset

- Padrão avançado; alinhar com APIs (`DefaultInterpolatedStringHandler`, …) na BCL.

## Próximo passo

[global-usings.md](global-usings.md) · [csharp-10-0-overview.md](csharp-10-0-overview.md)
