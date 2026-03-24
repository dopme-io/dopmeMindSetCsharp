# Suprimir emissão de `localsinit` (C# 9.0)

## Contexto

O atributo **`SkipLocalsInit`** (em conjunto com opções do projeto) permite **omitir** a instrução IL **`localsinit`** em métodos, **poupando** instruções em caminhos críticos. Os locais podem ficar **não inicializados** — só use quando o código garante escrita antes da leitura.

## Onde aplicar

Tipicamente em métodos marcados e revisados; alinhar com documentação Microsoft sobre **segurança** e **análise** do código gerado.

## Próximo passo

[module-initializers.md](module-initializers.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
