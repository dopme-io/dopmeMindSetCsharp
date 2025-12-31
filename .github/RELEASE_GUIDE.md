# Release Guide

Este guia explica como criar releases automatizadas para o projeto MindSetCSharp.

## Workflows Disponíveis

### 1. Release Workflow (`release.yml`)

**Trigger:** Criação de tags de versão (formato `v*.*.*`)

Este workflow é executado automaticamente quando você cria e envia uma tag de versão para o repositório.

**O que faz:**
- Faz build do projeto
- Executa testes
- Publica o aplicativo console para múltiplas plataformas (Windows, Linux, macOS)
- Cria arquivos ZIP com os executáveis
- Gera changelog automático
- Cria uma release no GitHub com os artefatos

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
- Valida o formato da versão
- Verifica se a tag já existe
- Faz build e testes
- Publica para múltiplas plataformas (incluindo macOS ARM64)
- Cria e envia a tag automaticamente
- Cria a release com changelog

### 3. Create Version Tags Workflow (`create-tags.yml`)

**Trigger:** Executado manualmente através do GitHub Actions

Este workflow facilita a criação de tags para as versões 1.0.0 e 2.0.0.

**Como usar:**
1. Vá para `Actions` no GitHub
2. Selecione `Create Version Tags`
3. Clique em `Run workflow`
4. Marque as versões que deseja criar (v1.0.0 e/ou v2.0.0)
5. Clique em `Run workflow`

**O que faz:**
- Cria as tags selecionadas
- Envia as tags para o repositório
- Automaticamente dispara o workflow de release

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

### Método 3: Usando o Workflow de Tags

1. Acesse: `https://github.com/dopme-io/UseMindCSharp/actions/workflows/create-tags.yml`
2. Clique em `Run workflow`
3. Selecione as versões que deseja criar
4. Execute

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
dotnet test --configuration Release
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
