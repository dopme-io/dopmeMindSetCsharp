# Restrição genérica `where T : unmanaged` (C# 7.3)

## Ideia

**C# 7.3** introduziu a restrição **`unmanaged`** em parâmetros de tipo: **`T`** tem de ser um tipo **valor** cujos campos são **apenas** tipos não referenciados (sem referências a objetos geridos no layout), permitindo **ponteiro** a `T*` em contextos **`unsafe`** com garantias de tipo.

Isto é o núcleo de “**mais restrições genéricas**” nesta versão: **blittable** / interopável de forma previsível.

## Exemplo ilustrativo

```csharp
unsafe static void Zero<T>(T* p, int count) where T : unmanaged
{
    for (int i = 0; i < count; i++)
        p[i] = default;
}
```

## Mindset

- **Ponteiros** e buffers tipados sem **`object`** ou **`string`** no meio do struct.
- Combine com **`Span<T>`**, **`stackalloc`**, e APIs de baixo nível documentadas na sua plataforma alvo.

## Ver também

- [generics.md](generics.md) (C# 2.0)
- [generic-constraints-7-2-note.md](generic-constraints-7-2-note.md) (nota 7.2 vs 7.3)
- [csharp-7-3-overview.md](csharp-7-3-overview.md)
