# Literais UTF-8 (C# 11.0)

## Contexto

O sufixo **`u8`** produz **`ReadOnlySpan<byte>`** (ou tipos compatíveis) com conteúdo **UTF-8** conhecido em **tempo de compilação**, evitando alocar `string` intermédia quando o consumidor espera bytes.

## O que praticar

```csharp
ReadOnlySpan<byte> utf8 = "Olá"u8;
```

## Próximo passo

[interpolated-newlines.md](interpolated-newlines.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
