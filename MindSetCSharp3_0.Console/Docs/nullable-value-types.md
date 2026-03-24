# Tipos valor anuláveis — nullable value types (C# 2.0)

## Contexto

Em C# 1.x, **tipos valor** (`int`, `bool`, `DateTime`, …) **não** podiam representar “sem valor”. C# 2.0 introduziu **`T?`** (sintaxe para **`Nullable<T>`**) para `struct`, permitindo algo como **`int?`** com **`null`**.

**Tipos referência** já eram anuláveis; o foco aqui é **valor opcional**.

## O que implementar / praticar

1. Modelar campos opcionais: `int? idade = null`.
2. Usar **`HasValue`**, **`Value`**, ou padrão **`??`** / **`?.`** (posterior) com cuidado.
3. **Lifting** de operadores: expressões com `int?` combinam regras definidas pela linguagem.

## Exemplo mínimo

```csharp
int? opcional = null;
opcional = 42;
if (opcional.HasValue)
{
    System.Console.WriteLine(opcional.Value);
}
```

## Mindset

- Distinguir **zero** de **desconhecido** (ex.: base de dados com coluna opcional).
- Com **nullable reference types** (C# 8+) o significado de `null` em `string` muda de aviso; aqui o foco é **`Nullable<T>`** para structs.

## Próximo passo

[iterators.md](iterators.md)
