# *Records* (C# 9.0)

## Contexto

**Records** (`record` / `record class`) oferecem sintaxe breve para **tipos referência** cuja **igualdade** segue **semântica por valor** (comparação por conteúdo, não por identidade de referência por defeito). São adequados a **modelos de dados** com pouco comportamento.

## O que praticar

```csharp
public record Pessoa(string Nome, int Idade);

var a = new Pessoa("Ana", 30);
var b = new Pessoa("Ana", 30);
Console.WriteLine(a == b); // True (igualdade estrutural)

var c = a with { Idade = 31 }; // cópia com mutação não destrutiva
```

- `record struct` (C# 10+) é outra variante; aqui o foco é **`record`** / **`record class`** em **C# 9**.

## Mindset — próximo passo

[init-only-setters.md](init-only-setters.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
