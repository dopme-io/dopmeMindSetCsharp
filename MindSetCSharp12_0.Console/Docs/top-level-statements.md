# Instruções de nível superior (*top-level statements*) (C# 9.0)

## Contexto

Pode escrever instruções **directamente** num ficheiro `.cs` (normalmente **um** ficheiro por projeto com este estilo). O compilador gera **`Main`** e classe contentora — **sem** obrigatoriamente declarar `namespace`, `Program` e `static void Main()`.

## O que saber

- Apenas **um** ficheiro do projeto deve ter instruções de nível superior (regra do compilador).
- `args` está disponível como parâmetros de linha de comando implícitos.
- Útil para scripts e programas curtos; projectos maiores podem manter `Main` explícito por clareza.

## Próximo passo

[pattern-relational-logical.md](pattern-relational-logical.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
