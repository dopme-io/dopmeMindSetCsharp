# Versão da linguagem (`LangVersion`) e `-refout` / `-refonly` (C# 7.1)

## `LangVersion` no projeto

A partir do **C# 7.1**, a documentação e as ferramentas **.NET** consolidaram a forma de **fixar a versão da linguagem** no ficheiro de projeto, por exemplo:

```xml
<PropertyGroup>
  <LangVersion>7.1</LangVersion>
  <!-- Outros valores comuns: 7.3, 8.0, 9.0, 10.0, 11, 12, latest, preview, default -->
</PropertyGroup>
```

- **`default`** (ou omitir) — usa a versão predefinida associada ao **target framework** / SDK.
- **`latest`** — a mais recente estável que o compilador suporta (o significado exato depende da versão do SDK).
- Fixar **`7.1`** (ou outra) garante **comportamento reprodutível** em CI e em máquinas com SDKs diferentes.

Este repositório usa normalmente **`LangVersion` alto** nos `.csproj` dos consoles MindSet para permitir exemplos com o compilador atual; os textos em `Docs/` descrevem funcionalidades **por versão histórica** da linguagem.

## Reference assemblies: `-refout` e `-refonly`

O compilador **Roslyn** passou a expor opções para gerar **reference assemblies**:

- **`-refonly`** — emite **apenas** um assembly de referência (metadados públicos), sem IL executável completa para implementação privada.
- **`-refout:<caminho>`** — emite o assembly de referência para o caminho indicado **em conjunto** com a compilação normal (conforme a configuração).

Estes artefactos são úteis para **compilação em camadas** (por exemplo, um pacote que só expõe API pública), **builds incrementais** e ferramentas que consomem **apenas a superfície pública**.

No **SDK .NET** moderno, propriedades MSBuild como **`ProduceReferenceAssembly`** (e relacionadas) mapeiam este comportamento; consulte a documentação da sua versão do SDK para a sintaxe exata.

## Mindset

- **`LangVersion`** é **governação** do código: alinha equipa, CI e bibliotecas.
- **Reference assemblies** são **otimização e contrato**: separam “o que é público” da implementação, útil em repositórios grandes.

## Ver também

- [csharp-7-1-overview.md](csharp-7-1-overview.md)
