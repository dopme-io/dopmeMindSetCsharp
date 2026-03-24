# C# 4.0 — visão geral (abril 2010)

## Contexto

**C# 4.0** saiu com o **Visual Studio 2010** e o **.NET Framework 4**. Trouxe várias melhorias pontuais:

- **Interop COM**: **tipos de interop incorporados** (*embedded interop types*, também conhecidos por **NoPIA** — *No Primary Interop Assembly*) aliviavam a dor de distribuir e versionar assemblies de interop gerados para Office e outros componentes COM.
- **Genéricos**: **covariância e contravariância** em **interfaces** (e delegados) com anotações **`out`** e **`in`** — poderoso, por vezes “académico”, muito valorizado por autores de **bibliotecas** e frameworks.
- **Métodos**: **parâmetros opcionais** (valores por defeito) e **argumentos nomeados** reduzem sobrecargas repetitivas e melhoram legibilidade nas chamadas.

Nenhuma destas três áreas muda sozinha o paradigma da linguagem da mesma forma que a quarta.

## A grande novidade: `dynamic`

A funcionalidade mais marcante foi a palavra-chave **`dynamic`**: o compilador **adianta** a verificação de tipos para a **runtime**, via **DLR** (*Dynamic Language Runtime*). Isto aproxima alguns padrões de linguagens **dinamicamente tipadas** (por analogia com JavaScript), com o custo de **menos garantias em tempo de compilação** e potencial para **erros só em execução**.

Pode escrever-se, por exemplo, `dynamic x = "a string"` e depois combinar `x` com outros valores: o que acontece depende da **resolução dinâmica** em runtime — por vezes útil (COM, reflexão, APIs dinâmicas), por vezes **frágil** se não houver disciplina.

## Mindset

- **`dynamic`**: poder e flexibilidade **versus** segurança estática — usar com critério e limites claros (fronteiras bem definidas).
- **Variança `out`/`in`**: modelar “posso devolver algo **mais derivado**” / “posso aceitar algo **mais base**” de forma **segura** nas interfaces genéricas.

## Próximo passo

[dynamic-binding.md](dynamic-binding.md)
