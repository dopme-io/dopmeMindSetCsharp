# Release Guide

Este guia explica como criar releases automatizadas para o projeto MindSetCSharp.

## Workflows Disponíveis

### 1. Release Workflow (`release.yml`)

**Trigger:** Criação de tags de versão (formato `v*.*.*`)

Este workflow é executado automaticamente quando você cria e envia uma tag de versão para o repositório.

**O que faz:**
- Restaura e compila a solução `MindSetCSharp.sln`
- **Deteta automaticamente** todos os `.csproj` com `<OutputType>Exe</OutputType>` (cada projeto console / nova edição na solução)
- Publica cada um como **self-contained** para `win-x64`, `linux-x64`, `osx-x64` e `osx-arm64`
- Gera um ZIP por projeto e por RID (`MindSetCSharp-<PastaDoProjeto>-v<versão>-<rid>.zip`)
- Gera changelog e cria a release no GitHub

**Nota:** Este workflow **não** corre quando a tag foi enviada pelo workflow *Manual Release* (`github-actions[bot]`), para evitar release duplicado. Tags criadas por si (push local ou UI) disparam este fluxo normalmente.

### 2. Manual Release Workflow (`manual-release.yml`)

**Trigger:** Executado manualmente através do GitHub Actions

Este workflow permite criar releases de forma manual através da interface do GitHub.

**Como usar:**
1. Vá para `Actions` no GitHub
2. Selecione `Manual Release`
3. Clique em `Run workflow`
4. Insira a versão (ex: `1.0.0` ou `2.0.0`)
5. Escolha se é uma pre-release (opcional)
6. Clique em `Run workflow`

**O que faz:**
- Valida o formato da versão e se a tag ainda não existe
- Restaura, compila e publica **todos** os projetos console (mesma deteção que `release.yml`)
- Gera ZIPs self-contained (Windows, Linux, macOS Intel e Apple Silicon)
- Cria e envia a tag `vX.Y.Z` e publica a **release** com os artefactos (evita duplicar com `release.yml` graças ao filtro de actor no outro workflow)

### 3. Create Version Tag (`create-tags.yml`)

**Trigger:** Manual (`workflow_dispatch`)

Cria **apenas** uma tag `vX.Y.Z` no commit atual (input: versão `1.0.0`). **Não** gera ZIPs nem release — use quando quiser só marcar o histórico, ou faça push da tag **a partir do seu ambiente** para disparar o `release.yml` com o seu utilizador.

**Como usar:** Actions → *Create Version Tag* → Run workflow → indique `X.Y.Z`.

## Como Criar Releases

### Método 1: Usando Tags Manualmente

```bash
# Criar tag localmente
git tag -a v1.0.0 -m "Release version 1.0.0"

# Enviar tag para GitHub
git push origin v1.0.0
```

### Método 2: Usando o Workflow Manual

1. Acesse: `https://github.com/dopme-io/UseMindCSharp/actions/workflows/manual-release.yml`
2. Clique em `Run workflow`
3. Preencha a versão desejada
4. Execute

### Método 3: Apenas criar tag (sem artefactos)

1. Acesse o workflow `create-tags.yml` em Actions
2. Indique a versão `X.Y.Z` e execute

Para release com ZIPs, prefira o **Método 1** (push de tag pelo seu utilizador) ou o **Método 2** (*Manual Release*).

## Estrutura de Versão

O projeto utiliza [Semantic Versioning](https://semver.org/):

- **MAJOR.MINOR.PATCH** (ex: `1.0.0`, `2.0.0`)
- Tags devem ser prefixadas com `v` (ex: `v1.0.0`)

## Plataformas Suportadas

Os releases incluem executáveis para:

- **Windows x64** - Testado em Windows 10/11
- **Linux x64** - Testado em Ubuntu 20.04+
- **macOS x64** - Intel Macs
- **macOS ARM64** - Apple Silicon (M1/M2/M3)

Todos os executáveis são **self-contained** (incluem o runtime do .NET).

## Artefatos da Release

Cada release inclui:

- Arquivos ZIP para cada plataforma
- Changelog automático
- Documentação de instalação
- Links para documentação completa

## Troubleshooting

### Tag já existe

Se a tag já existe:
```bash
# Deletar tag local
git tag -d v1.0.0

# Deletar tag remota
git push origin :refs/tags/v1.0.0
```

### Build falhou

1. Verifique os logs no GitHub Actions
2. Teste localmente:
```bash
dotnet build --configuration Release
```

### Workflow não disparou

1. Verifique se a tag foi enviada: `git push origin v1.0.0`
2. Verifique os triggers no arquivo `.github/workflows/release.yml`
3. Certifique-se que a tag segue o formato `v*.*.*`

## Exemplo de Fluxo Completo

```bash
# 1. Fazer as alterações necessárias
git add .
git commit -m "Prepare for release v1.0.0"
git push origin main

# 2. Criar e enviar a tag
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0

# 3. O workflow será executado automaticamente
# 4. Aguarde a conclusão em: https://github.com/dopme-io/UseMindCSharp/actions
# 5. A release estará disponível em: https://github.com/dopme-io/UseMindCSharp/releases
```

## Próximos Passos

Para criar as releases das versões existentes:

1. **Para v1.0.0:**
   - Use o workflow `Create Version Tags` e marque `create_v1`
   - OU execute: `git tag -a v1.0.0 -m "Release version 1.0.0" && git push origin v1.0.0`

2. **Para v2.0.0:**
   - Use o workflow `Create Version Tags` e marque `create_v2`
   - OU execute: `git tag -a v2.0.0 -m "Release version 2.0.0" && git push origin v2.0.0`

Após criar as tags, os releases serão criados automaticamente!
