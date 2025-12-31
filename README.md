<div align="center">
  <img width="263" height="182" alt="dopme io" src="https://github.com/dopme-io/dopmeRepo/blob/main/assests/Use%20Mindset%20com%20CSharp.png" />
  </br>
  <img width="663" height="69" src="https://github.com/dopme-io/dopmeRepo/blob/main/assests/MindSet%20CSharp.png" />

  [![.NET](https://github.com/dopme-io/UseMindCSharp/actions/workflows/dotnet.yml/badge.svg)](https://github.com/dopme-io/UseMindCSharp/actions/workflows/dotnet.yml)
  ![Versão](https://img.shields.io/badge/.NET-10.0-blue)
  
  Repositório educacional focado em fundamentos de programação C# com abordagem Mindset. Explora conceitos essenciais através de uma mentalidade eficaz para o desenvolvimento de software em C#.
</div>


---

## 🗂 Índice

- [Sobre](#-sobre)
- [Tecnologias](#️-tecnologias)
- [Arquitetura](#-arquitetura)
- [Instalação](#-instalação)
- [Uso](#️-uso)
- [Estrutura dos Módulos](#-estrutura-dos-módulos)
- [Testes](#-testes)
- [Contribuição](#-contribuição)
- [Licença](#-licença)
- [Contato](#-contato)

---

## 📌 Sobre
Este projeto faz parte do ecossistema `dopme-io` e tem como objetivo principal explorar a base fundamental da programação em C# através da abordagem Mindset. A ênfase está em não apenas aprender a sintaxe da linguagem, mas também em adotar uma mentalidade eficaz para o desenvolvimento de software.

### O que você aprenderá:

- **Mentalidade Orientada a Objetos**: Como pensar em termos de classes e objetos para criar sistemas modulares e reutilizáveis.
- **Design de Código Limpo**: Práticas para escrever código claro e sustentável, incluindo princípios como a responsabilidade única e a inversão de dependência.
- **Estruturas e Algoritmos**: Compreensão de como aplicar estruturas de dados e algoritmos de maneira eficiente e adequada.
- **Boas Práticas de Programação**: Técnicas e padrões para resolver problemas comuns e evitar armadilhas típicas.
- **Tratamento de Exceções e Depuração**: Como adotar uma mentalidade de resolução de problemas e tratamento de exceções para garantir a robustez do código.
- **Eficiência e Performance**: Abordagens para escrever código que não apenas funciona, mas também é eficiente e bem otimizado.

---

## 🛠️ Tecnologias

- [C# 13](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-13)
- [.NET 10 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/10.0)
- [Visual Studio](https://visualstudio.microsoft.com/pt-br/)
- [VS Code](https://code.visualstudio.com/)

---

## 🧱 Arquitetura
- Arquitetura modular baseada em bibliotecas de classes.
- Separação clara de responsabilidades por domínio (Módulos).
- Aplicação console demonstrativa com acesso a todos os módulos educacionais.


```
📁 src/
├── MindSetCSharp.Console/          # Aplicação console demonstrativa
│   ├── Program.cs                  # Entry point com todos os módulos
│   └── MindSetCSharp.Console.csproj
└── MindSetCSharp.Core/             # Biblioteca de classes principal
    ├── Produtivo/                  # Dicas e técnicas de produtividade
    ├── Bastidores/                 # Internos da execução .NET
    ├── Objetos/                    # Fundamentos de POO
    ├── Tipos/                      # Tipos primitivos e complexos
    ├── Referencias/                # Trabalho com referências
    ├── Encapsulamento/             # Princípios de encapsulamento
    ├── Herança/                    # Conceitos de herança
    ├── Interface/                  # Uso de interfaces
    ├── Classes/                    # Criação e uso de classes
    ├── Enumerações/                # Definição e uso de enums
    ├── Coleções/                   # Arrays, listas, dicionários
    ├── Arquivos/                   # Manipulação de arquivos
    ├── Exceções/                   # Tratamento de exceções
    ├── Eventos/                    # Sistema de eventos
    ├── Delegates/                  # Uso de delegados
    ├── Revisão/                    # Exercícios e desafios
    ├── Controles/                  # Controles de interface
    ├── Gráficos/                   # Criação de gráficos
    ├── LINQ/                       # Language Integrated Query
    └── MindSetCSharp.Core.csproj
```

📘 **Documentação Técnica Completa**: [DOCUMENTATION.md](DOCUMENTATION.md)

---

## 🚀 Instalação

### Requisitos
- .NET 10 SDK instalado ([Download aqui](https://dotnet.microsoft.com/download))

### Clonar o repositório
```bash
git clone https://github.com/dopme-io/UseMindCSharp.git
```

### Entrar no diretório
```bash
cd UseMindCSharp
```

### Restaurar dependências
```bash
dotnet restore
```

---

## ▶️ Uso

### Build da solução
```bash
dotnet build
```

### Executar aplicação console
```bash
dotnet run --project MindSetCSharp.Console
```

### Build em modo Release
```bash
dotnet build --configuration Release
```

---

## 📚 Estrutura dos Módulos

### **/Produtivo**:
Dicas e técnicas para otimizar a produtividade no desenvolvimento com C#. Inclui práticas recomendadas para escrever código mais eficiente e como melhorar seu fluxo de trabalho de programação.

### **/Bastidores**:
Exploração dos detalhes internos da execução de código C# e da plataforma .NET. Esta seção aborda o que acontece "nos bastidores" durante a compilação e execução do código.

### **/Objetos**:
Fundamentos da programação orientada a objetos em C#. Inclui criação e manipulação de objetos, e como utilizar objetos para estruturar e organizar seu código.

### **/Tipos**:
Descrição dos tipos de dados em C#, incluindo tipos primitivos e tipos complexos. Explora a diferença entre tipos de valor e tipos de referência.

### **/Referencias**:
Como trabalhar com referências em C#, abordando conceitos de referências de objetos, comparação e manipulação de referências.

### **/Encapsulamento**:
Princípios de encapsulamento e como aplicá-los para proteger dados e abstrair detalhes de implementação em suas classes.

### **/Herança**:
Conceitos e práticas de herança em C#, incluindo como criar classes derivadas e a importância da herança para reutilização e extensão de código.

### **/Interface**:
Utilização de interfaces para definir contratos em C#. Inclui como criar e implementar interfaces para promover a flexibilidade e a interoperabilidade no código.

### **/Classes**:
Criação e uso de classes em C#. Inclui a definição de propriedades, métodos e construtores, e a importância das classes na programação orientada a objetos.

### **/Enumerações**:
Introdução às enumerações em C#, como definir e utilizar enums para representar conjuntos de valores nomeados e melhorar a legibilidade do código.

### **/Coleções**:
Trabalhando com diferentes tipos de coleções em C#, como arrays, listas, dicionários e conjuntos. Exemplos de uso e quando escolher cada tipo de coleção.

### **/Arquivos**:
Manipulação de arquivos em C#. Inclui leitura e escrita de arquivos, além de boas práticas para gerenciar dados persistentes.

### **/Exceções**:
Tratamento de exceções em C#. Como capturar, lançar e gerenciar erros para garantir que seu código seja robusto e confiável.

### **/Eventos**:
Uso de eventos para criar sistemas de notificação e comunicação entre objetos em C#. Inclui como definir e manipular eventos para responder a alterações e ações.

### **/Delegates**:
Conceito e utilização de delegados em C#. Como criar e usar delegados para implementar métodos que podem ser passados como parâmetros e armazenados em variáveis.

### **/Revisão**:
Revisão dos conceitos fundamentais cobertos nas seções anteriores. Inclui exercícios e desafios para reforçar o aprendizado e testar o conhecimento adquirido.

### **/Controles**:
Trabalhando com controles em aplicações de desktop e web usando C#. Exemplos de criação e manipulação de diferentes tipos de controles e componentes de interface.

### **/Gráficos**:
Criação e manipulação de gráficos em C#. Inclui o uso de bibliotecas e frameworks para desenhar e visualizar dados graficamente.

### **/LINQ**:
Utilização de LINQ (Language Integrated Query) para consultar e manipular dados em coleções e outras fontes de dados. Inclui exemplos de consultas LINQ e suas aplicações.

---

## ✅ Testes

### Rodar todos os testes
```bash
dotnet test
```

### Teste com coverage
```bash
dotnet test /p:CollectCoverage=true
```

---

## 🤝 Contribuição
Este projeto é mantido pela equipe interna da organização `dopme-io`.

Se você é membro da organização:

- Siga o [guia de contribuição](./DOCUMENTATION.md)
- Mantenha o padrão de código e documentação.

Se este for um repositório open source, contribuições externas são bem-vindas mediante revisão prévia.

---

## 📄 Licença
Este projeto está licenciado sob a [MIT License](./LICENSE).

---

## 📬 Contato
Caso tenha dúvidas ou sugestões, entre em contato:

- **Email**: [daniloopinheiro@dopme.io](mailto:daniloopinheiro@dopme.io)
- **LinkedIn**: [dopme-io](https://www.linkedin.com/company/dopme-io/)
- **YouTube**: [dopme](https://www.youtube.com/@dopme-io)
- **Contato**: [Whatsapp Business](https://wa.me/5511964952665)

---

*Este repositório é ideal para desenvolvedores que desejam não apenas aprender C#, mas também adotar uma abordagem mental e prática para resolver problemas de programação e construir soluções eficazes e escaláveis.*

