# Tipos de retorno covariantes (C# 9.0)

## Contexto

Um método `override` pode declarar um tipo de retorno **mais derivado** que o método virtual na classe base (`return type covariance`). Isso alinha com **hierarquias de records** e APIs que estreitam o tipo concreto devolvido.

## Exemplo conceitual

```csharp
public class Widget { }

public abstract class Factory
{
    public abstract object Create();
}

public class WidgetFactory : Factory
{
    public override Widget Create() => new(); // covariante face a object
}
```

## Próximo passo

[extension-getenumerator-foreach.md](extension-getenumerator-foreach.md) · [csharp-9-0-overview.md](csharp-9-0-overview.md)
