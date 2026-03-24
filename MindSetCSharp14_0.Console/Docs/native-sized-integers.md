# Inteiros de tamanho nativo (`nint` / `nuint`) (C# 9.0)

## Contexto

**`nint`** e **`nuint`** modelam inteiros com largura da **CPU alvo** (análogos a ponteiros de tamanho nativo em interop e código de desempenho). São úteis em cenários de **computação de alto desempenho** e **P/Invoke**.

## Notas

- O tipo em tempo de execução depende do alvo (`System.IntPtr` / `System.UIntPtr` em muitos casos).
- Combine com cuidado com código verificado / unsafe conforme o cenário.

## Próximo passo

[function-pointers.md](function-pointers.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
