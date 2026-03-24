# Ligação dinâmica — `dynamic` (C# 4.0)

## Contexto

O tipo **`dynamic`** instrui o compilador a tratar as operações como **ligação adiada** (*late binding*): em tempo de execução, o runtime (via **DLR**) tenta resolver membros, conversões e operadores. **Erros que antes seriam de compilação** podem surgir só como **`RuntimeBinderException`** (ou comportamentos inesperados).

Isto **não** torna C# uma linguagem dinâmica de ponta a ponta: a maior parte do código continua **estaticamente tipado**; `dynamic` é uma **área delimitada** onde se aceita menos verificação estática.

## O que praticar

1. Atribuição: `dynamic d = 1; d = "texto";` — o **valor** muda; o uso de membros depende do **tipo em runtime**.
2. Comparar com **`object`**: com `object` é preciso **cast** explícito para chamar membros específicos; com `dynamic` o compilador **não** exige cast na escrita, mas a resolução falha em runtime se não existir membro compatível.
3. **COM** e APIs legadas: cenários históricos típicos de `dynamic` (junto com interop).

## Exemplo — risco ilustrativo

```csharp
dynamic x = "a string";
// int n = x + 6;  // pode compilar, mas em runtime o resultado depende
// das regras do DLR / overloads; cenários inválidos geram RuntimeBinderException
```

Prefira **tipos estáticos** e **`var`** (inferência **estática**) quando a forma do dado é conhecida no desenho.

## Mindset

Cada `dynamic` é um **contrato implícito** com o runtime: ganha-se flexibilidade, perde-se a rede de segurança do compilador. Limite a superfície (APIs, camadas de integração).

## Próximo passo

[named-optional-arguments.md](named-optional-arguments.md)
