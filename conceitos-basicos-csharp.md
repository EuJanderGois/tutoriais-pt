
# Conceitos Básicos de CSharp

## O que vou aprender?

- [[Conceitos Básicos de CSharp#O que é C ?]]
- [[Conceitos Básicos de CSharp#Variáveis]]
- [[Conceitos Básicos de CSharp#Objetos]]
- [[Conceitos Básicos de CSharp#Namespaces]]
- [[Conceitos Básicos de CSharp#Convenção de Nomes e Cases]]
- [[Conceitos Básicos de CSharp#Loops]]
- [[Conceitos Básicos de CSharp#Condições]]

## O que é C# ?
C# (pronuncia-se "C sharp") é uma linguagem de programação moderna, orientada a objetos, desenvolvida pela Microsoft como parte da plataforma .NET. Foi criada por Anders Hejlsberg e sua equipe em 2000.

C# é uma linguagem de alto nível, que combina a facilidade de uso e a eficiência da linguagem C++ com a segurança e a plataforma gerenciada do .NET Framework. Ela é amplamente utilizada para desenvolver aplicações Windows, web, mobile e games.

Algumas das principais características do C# incluem:

- **Orientação a objetos**: C# suporta conceitos de programação orientada a objetos, como classes, objetos, herança, polimorfismo e encapsulamento.
- **Tipagem forte**: C# é uma linguagem de tipagem forte, o que significa que o compilador verifica os tipos de dados em tempo de compilação, ajudando a prevenir erros.
- **Garbage collection**: O .NET Framework inclui um garbage collector, que automaticamente gerencia a memória e evita vazamentos de memória.
- **Compatibilidade com o .NET Framework**: C# é projetada para trabalhar em conjunto com o .NET Framework, que fornece uma ampla gama de bibliotecas e APIs para desenvolver aplicações.

Em resumo, C# é uma linguagem de programação poderosa e flexível, ideal para desenvolver aplicações de alta qualidade e escalabilidade.

## Variáveis

Em C#, uma variável é um nome dado a um local de memória que armazena um valor. Existem dois tipos de variáveis: **valor** e **referência**.

- **Valor**: armazena um valor primitivo, como um número ou um caractere.
- **Referência**: armazena uma referência a um objeto.

Exemplo de declaração de variáveis:

```csharp
int x = 10; // variável de valor
string nome = "João"; // variável de valor
Carro meuCarro = new Carro(); // variável de referência
```

## Objetos

Em C#, um objeto é uma instância de uma classe. Uma classe é um modelo que define as propriedades e métodos de um objeto.

Exemplo de criação de um objeto:

```csharp
public class Carro {
    public string marca;
    public string modelo;
    public int ano;

    public Carro(string marca, string modelo, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.ano = ano;
    }
}

Carro meuCarro = new Carro("Ford", "Focus", 2015);
```

## Namespaces

Um namespace é um espaço de nomes que organiza as classes e outros tipos de C#. Ele ajuda a evitar conflitos de nomes entre classes e tipos.

Exemplo de uso de namespace:

```csharp
using System;

namespace MeuNamespace {
    public class MinhaClasse {
        // código da classe
    }
}
```

## Convenção de Nomes e Cases

Em C#, é comum seguir as seguintes convenções de nomes e cases:

- **PascalCase**: primeira letra de cada palavra em maiúscula (ex: `MinhaClasse`)
- **camelCase**: primeira letra da primeira palavra em minúscula, e primeira letra de cada palavra subsequente em maiúscula (ex: `minhaVariavel`)
- **Uppercase**: todas as letras em maiúscula (ex: `CONSTANTE`)

## Loops

Um loop é uma estrutura de controle que permite executar um bloco de código repetidamente.

Exemplos de loops em C#:

- **for**: loop que executa um bloco de código enquanto uma condição for verdadeira.

```csharp
for (int i = 0; i < 10; i++) {
    Console.WriteLine(i);
}
```

- **while**: loop que executa um bloco de código enquanto uma condição for verdadeira.

```csharp
int i = 0;
while (i < 10) {
    Console.WriteLine(i);
    i++;
}
```

- **foreach**: loop que executa um bloco de código para cada item em uma coleção.

```csharp
string[] nomes = { "João", "Maria", "Pedro" };
foreach (string nome in nomes) {
    Console.WriteLine(nome);
}
```

## Condições

Uma condição é uma estrutura de controle que permite executar um bloco de código se uma condição for verdadeira.

Exemplos de condições em C#:

- **if**: executa um bloco de código se uma condição for verdadeira.

```csharp
int x = 10;
if (x > 5) {
    Console.WriteLine("x é maior que 5");
}
```

- **if-else**: executa um bloco de código se uma condição for verdadeira, e outro bloco de código se a condição for falsa.

```csharp
int x = 10;
if (x > 5) {
    Console.WriteLine("x é maior que 5");
} else {
    Console.WriteLine("x é menor ou igual a 5");
}
```

- **switch**: executa um bloco de código com base no valor de uma variável.

```csharp
int diaSemana = 2;
switch (diaSemana) {
    case 1:
        Console.WriteLine("Segunda-feira");
        break;
    case 2:
        Console.WriteLine("Terça-feira");
        break;
    // ...
}
```

Esses são os conceitos básicos do C#. Espero que isso tenha ajudado!
