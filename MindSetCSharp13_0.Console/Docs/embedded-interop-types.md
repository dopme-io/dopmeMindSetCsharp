# Tipos de interop incorporados — NoPIA (C# 4.0 / VS 2010)

## Contexto

Integrar com **COM** (ex.: automação **Office**) historicamente implicava **Primary Interop Assemblies** (PIAs) — assemblies .NET grandes que tinham de ser **instalados** ou **empacotados** com a aplicação. **C# 4.0** e o **Visual Studio 2010** popularizaram a opção **Embed Interop Types** (*tipos de interop incorporados*): apenas os **tipos e membros realmente usados** são embutidos na sua assembly, reduzindo dependências e conflitos de versão do PIA completo.

Também se refere a isto como **NoPIA** (*No Primary Interop Assembly*).

## O que praticar

1. Em projetos clássicos (.NET Framework, COM Reference), propriedade **Embed Interop Types = True** na referência interop.
2. Diferença face a copiar o PIA inteiro para a pasta de saída.
3. Em **SDK-style** / .NET moderno, interop COM costuma seguir **outros mecanismos** (geração de código, `ComImport`, Source Generators): o **conceito** de “embutir só o necessário” permanece relevante para entender a motivação de 2010.

## Mindset

Menos **fricção de implantação** em cenários Office/COM; ainda hoje, prefira **fronteiras explícitas** entre código gerido e COM.

## Próximo passo

[csharp-4-0-overview.md](csharp-4-0-overview.md) (reler) ou tabela **C# 3.0** no [README.md](README.md).
