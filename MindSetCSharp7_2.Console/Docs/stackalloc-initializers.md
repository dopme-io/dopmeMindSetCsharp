# Inicializadores em `stackalloc` (C# 7.2)

## Ideia

Em **C# 7.2**, pode-se **inicializar** buffers criados com **`stackalloc`** na mesma expressão, em vez de atribuir elemento a elemento depois.

## Exemplo

```csharp
Span<int> digits = stackalloc int[3] { 1, 2, 3 };
```

(Com **`Span<T>`** e tipos relacionados, o padrão típico é alocação na stack com conteúdo imediato — útil em caminhos quentes sem heap.)

## Mindset

- Menos código repetitivo e menos risco de esquecer um índice ao preencher.
- `stackalloc` continua sujeito a **limites de stack** e a regras do compilador para **tamanho** e **segurança**.

## Ver também

- [ref-struct.md](ref-struct.md)
- [csharp-7-2-overview.md](csharp-7-2-overview.md)
