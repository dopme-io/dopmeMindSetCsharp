# `ref readonly` em retornos de método (C# 7.2)

## Ideia

Um método pode devolver **`ref readonly T`**: o valor é devolvido **por referência**, mas os **callers** não podem escrever através dessa referência — apenas **ler**. Útil para expor **slots** internos (por exemplo, em tipos estilo **`Span`** / coleções) sem cópia e sem mutação.

## Exemplo ilustrativo

```csharp
ref readonly int GetRefReadonly(ref int x) => ref x;
```

(Em APIs reais, o padrão aparece muito em **indexadores** e acessores otimizados.)

## Mindset

- **Partilha de vista** só leitura sobre armazenamento existente.
- Versões posteriores refinam regras e padrões; mantenha **APIs** documentadas quanto ao **tempo de vida** da referência.

## Ver também

- [ref-locals-returns.md](ref-locals-returns.md) (C# 7.0)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
