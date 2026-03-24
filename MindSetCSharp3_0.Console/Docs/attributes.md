# Atributos (C# 1.0)

## Contexto

**Atributos** adicionam **metadados** declarativos a assemblies, tipos, membros e parâmetros. Em tempo de execução, reflexão (`System.Reflection`) pode lê-los. C# 1.0 incluía atributos como `Obsolete`, `Serializable`, `DllImport` (interop), entre outros do BCL.

## O que implementar / praticar

1. Definir uma classe que derive de **`System.Attribute`**.
2. Nomear com sufixo **`Attribute`** (convenção); usar `[MeuAtributo]` no código (compilador aceita forma curta).
3. Controlar **alvos** com `[AttributeUsage(AttributeTargets.Class | AttributeTargets.Method)]`.
4. Ler atributos com `GetCustomAttributes` ou APIs equivalentes.

## Exemplo mínimo — atributo personalizado

```csharp
[AttributeUsage(AttributeTargets.Class)]
public class AuditoriaAttribute : Attribute
{
    private readonly string _modulo;

    public string Modulo
    {
        get { return _modulo; }
    }

    public AuditoriaAttribute(string modulo)
    {
        _modulo = modulo;
    }
}

[Auditoria("Vendas")]
public class Pedido
{
}
```

## Exemplo — consumo por reflexão (ideia)

```csharp
public static void ListarAuditoria(object alvo)
{
    var t = alvo.GetType();
    foreach (object a in t.GetCustomAttributes(typeof(AuditoriaAttribute), true))
    {
        AuditoriaAttribute au = a as AuditoriaAttribute;
        if (au != null)
        {
            System.Console.WriteLine("Módulo: " + au.Modulo);
        }
    }
}
```

(`GetCustomAttributes` em C# 1.0 devolvia `object[]`; o padrão acima é adaptado a sintaxe moderna.)

## Mindset

- Atributo = **dado declarativo** que ferramentas, frameworks ou o seu código consultam.
- Não coloque **lógica de negócio** dentro do construtor do atributo além do necessário para guardar parâmetros.

## Conclusão do roteiro C# 1.0

Voltar ao índice: [README.md](README.md).  
Releia os tópicos cruzando **classes**, **interfaces**, **delegates** e **eventos** — são o esqueleto da programação orientada a eventos na plataforma .NET clássica.
