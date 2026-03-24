# Conversão de *method group* para delegado (C# 11.0)

## Contexto

A **inferência** e as regras de conversão de **method group** para tipo **delegado** foram **melhoradas**, reduzindo casos em que era preciso *cast* explícito ou lambda desnecessária.

## O que praticar

Compare atribuições `Delegate d = M;` / `Func<...> f = M;` entre C# 10 e 11 em exemplos que antes falhavam.

## Próximo passo

[warning-wave-7.md](warning-wave-7.md) · [delegates.md](delegates.md) (base) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
