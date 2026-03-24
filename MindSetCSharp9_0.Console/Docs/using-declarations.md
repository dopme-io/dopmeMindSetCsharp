# Declarações `using` (C# 8.0)

## Ideia

Pode declarar um **`using`** com **âmbito** até ao **fim do bloco** envolvente, sem `using (...) { }` extra — o `Dispose` chama-se ao **sair** do bloco.

## Exemplo

```csharp
void M()
{
    using var stream = File.OpenRead("data.bin");
    // usar stream
} // Dispose aqui
```

## Mindset

- Menos **aninhamento**; mantenha blocos **curtos** para não alongar o tempo de vida do recurso.

## Ver também

- [csharp-8-0-overview.md](csharp-8-0-overview.md)
