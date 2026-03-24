# Tipos de referência anuláveis (C# 8.0)

## Ideia

Com **`<Nullable>enable</Nullable>`** (ou diretiva `#nullable`), o compilador distingue **referências que podem ser null** (`string?`) das que **não** devem ser null (`string`), com **avisos** quando o fluxo não garante segurança.

O ganho real aumenta quando as **bibliotecas** (`.NET Core` / BCL) incluem **anotações** de nullabilidade em APIs públicas.

## Exemplo

```csharp
string? FindName(int id) => id == 0 ? null : "x";

void Use(int id)
{
    string name = FindName(id)!; // ou verificação explícita
}
```

## Mindset

- **Contratos** de `null` como parte do tipo; **menos** `NullReferenceException** em tempo de execução com disciplina de equipa.

## Ver também

- [nullable-value-types.md](nullable-value-types.md) (C# 2.0 — `T?` valor)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
