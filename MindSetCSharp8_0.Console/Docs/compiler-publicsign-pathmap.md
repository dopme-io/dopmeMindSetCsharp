# Opções de compilador `-publicsign` e `-pathmap` (C# 7.3)

## `-publicsign`

Permite **assinatura pública** (“**OSS signing**”): o assembly inclui a **chave pública** e marca-se como assinado para **identidade** e **strong name**, sem exigir a **chave privada** no pipeline de build (adequado a repositórios abertos e builds reprodutíveis).

No **SDK .NET**, propriedades MSBuild como **`PublicSign`** mapeiam este comportamento — veja a documentação da sua versão.

## `-pathmap`

Fornece um **mapeamento** de prefixos de **diretórios de origem** (por exemplo, caminhos absolutos da máquina de build → caminhos lógicos estáveis), para que **PDBs**, **stack traces** e **diagnósticos** não vazem caminhos locais e os builds sejam mais **reprodutíveis**.

## Mindset

- **`-publicsign`**: identidade de pacote **open source** sem secret na CI.
- **`-pathmap`**: **privacidade** e **determinismo** em artefactos de debug.

## Ver também

- [langversion-ref-assemblies.md](langversion-ref-assemblies.md) (7.1 — outras opções de projeto/compilador)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
