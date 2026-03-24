# Tipos construídos geridos `unmanaged` (C# 8.0)

## Ideia

**C# 8.0** alarga **`unmanaged`**: tipos construídos como **`List<int>`** não são `unmanaged`, mas **`MyStruct<int>`** pode ser se **`T`** satisfizer `unmanaged` — regras mais flexíveis para **genéricos** e **interop**.

## Mindset

- **Ponteiros** e buffers tipados com mais **expressividade** genérica.

## Ver também

- [generic-constraint-unmanaged.md](generic-constraint-unmanaged.md) (C# 7.3)
- [csharp-8-0-overview.md](csharp-8-0-overview.md)
