# *Raw string literals* (C# 11.0)

## Contexto

**`""" … """`** (e variantes com múltiplos `"` para delimitadores mais longos) permitem strings **multilinha** com **menos escapes** — úteis para JSON, XML, SQL, caminhos Windows e texto com aspas.

## O que praticar

```csharp
var json = """
    {
      "ok": true
    }
    """;

var path = """C:\temp\file.txt""";
```

Compare com interpolação: prefixo `$"""` e chaves `{expr}` como em strings interpoladas habituais.

## Próximo passo

[utf8-string-literals.md](utf8-string-literals.md) · [csharp-11-0-overview.md](csharp-11-0-overview.md)
