# Programação Básica em C#

Aqui estão compiladas perguntas e respostas que cobrem a sintaxe básica e as construções fundamentais de C#.

## Perguntas e Respostas

### Quais partes compõe um programa em C#?

Um programa em C# é composto por:

- **Namespaces**: Organizam o código em contêineres lógicos.
- **Classes/Structs**: Define objetos e tipos de dados.
- **Métodos**: Define comportamentos e ações.
- **Variáveis**: Armazena dados e estados.
- **Diretivas Using**: Importa namespaces para serem usados no arquivo.
- **Atributos**: Fornecem metadados adicionais sobre o código.
- **Comentários**: Fornece descrições e anotações no código.

---
### Qual a finalidade do Using?

A diretiva `using` em C# tem duas finalidades principais:

#### Importação de Namespaces
Permite que você use classes, structs e outros tipos sem ter que referenciar o namespace completo. 

Exemplo: 
```csharp
using System;
```
Permitindo que você use o tipo `Console` sem ter que escrever `System.Console`.

#### Using Statement
Pode ser usado para garantir que os recursos, como arquivos ou conexões de rede, sejam liberados após o uso. 

Exemplo: 
```csharp
using (var stream = new FileStream("file.txt", FileMode.Open)) { ... }
```

---
### Qual a diferença entre uma variável e uma constante?

**Variável:**

- Uma variável é um nome dado a uma localização na memória onde um valor pode ser armazenado. Este valor pode ser modificado ao longo do tempo durante a execução do programa.
- As variáveis em .NET são fortemente tipadas, o que significa que o tipo de dados que a variável pode armazenar (int, double, string, etc.) é definido em tempo de compilação e não pode ser alterado em tempo de execução.
- No .NET, quando você define uma variável, você está na realidade criando uma instância de um tipo, que pode ser um tipo primitivo ou um tipo complexo (como uma classe ou uma estrutura).
- A variável tem um escopo determinado pelo contexto em que é declarada. Este escopo define onde a variável pode ser acessada. Ela pode ser local a um método, classe, namespace ou globalmente acessível se declarada como `public static`, por exemplo.

**Constante:**

- Uma constante, por outro lado, é um tipo especial de "variável" cujo valor é definido em tempo de compilação e não pode ser alterado em tempo de execução. Uma vez atribuído, o valor de uma constante permanece imutável.
- No .NET, você declara uma constante usando a palavra-chave `const` seguida por um tipo de dados e um valor inicial. Por exemplo, em C# você pode declarar uma constante inteira como `const int MaxSize = 10;`.
- As constantes são uma boa escolha quando você tem valores que são conhecidos em tempo de compilação e que não precisarão mudar durante a vida útil do programa. Isso pode incluir coisas como valores de configuração estática, valores matemáticos como pi, ou strings de formatação que são usadas em várias partes de um aplicativo.
- As constantes podem ser locais a um método ou podem ter um escopo mais amplo se forem declaradas ao nível da classe, mas mesmo assim elas não podem ser modificadas.

**Diferenças-chave:**

1. **Mutabilidade:** Variáveis podem ter seus valores alterados, enquanto constantes não.
2. **Tempo de Definição:** O valor de uma variável é atribuído em tempo de execução, enquanto o de uma constante é atribuído em tempo de compilação.
3. **Uso de Memória:** Como as constantes têm um valor imutável, elas podem ser otimizadas pelo compilador, que muitas vezes substitui referências à constante pelo seu valor literal durante a compilação, potencialmente economizando memória.
4. **Design de Aplicação:** Constantes são utilizadas para valores que não mudam e são conhecidos antes da execução do programa, enquanto variáveis são utilizadas para armazenar dados que podem mudar durante a execução.

Em resumo, a escolha entre usar uma variável ou uma constante depende da necessidade de alterar o valor após sua inicialização e do momento em que o valor é conhecido.

---
### Cite 3 nomes reservados que temos no C#

No C# (e na maioria das linguagens de programação), existem várias palavras-chave reservadas que servem como fundamentos da linguagem, e você não pode usá-las como identificadores (por exemplo, nomes de variáveis, classes, métodos, etc.) porque elas têm significados especiais para o compilador. Por exemplo:

#### class
A palavra-chave `class` é usada para declarar uma classe, que é uma das principais construções de programação orientada a objetos no C#. Uma classe é como um blueprint para criar objetos, que encapsulam dados e comportamento. Quando você declara uma classe, você está criando um novo tipo de dado que pode ser instanciado como objetos.

```csharp
public class Carro {
    public string Modelo;
    public void Acelerar() {
        // Método para acelerar o carro
    }
}
```

#### interface
A palavra-chave `interface` define uma interface em C#. Interfaces são contratos que definem um conjunto de métodos e propriedades que as classes ou estruturas que as implementam devem conter. Interfaces são importantes para criar código altamente modular e reutilizável e são uma parte central da programação orientada a objetos e do design de software.

```csharp
public interface IVeiculo {
    void Acelerar();
    void Frear();
}
```

#### void
A palavra-chave `void` é utilizada para especificar que um método não retorna um valor. Em C#, todo método pode retornar algum valor (como int, string, um objeto, etc.), mas quando um método não deve retornar nada, você usa o `void`.

```csharp
public void MostrarMensagem(string mensagem) {
    Console.WriteLine(mensagem);
}
```

---
### Quais formas temos de comentar código em C#?

1. **Comentários de linha única**: Utilizam duas barras inclinadas (`//`). Qualquer texto após `//` na mesma linha é tratado como comentário e, portanto, é ignorado pelo compilador. Por exemplo:

```csharp
// Isso é um comentário de linha única em C#
int numero = 5; // Isso também é um comentário
```

2. **Comentários de múltiplas linhas (ou comentários de bloco)**: São iniciados com `/*` e terminados com `*/`. Qualquer texto entre `/*` e `*/` será tratado como comentário, independentemente de quantas linhas ele abranja. Por exemplo:

```csharp
/* Este é um comentário de múltiplas linhas
   e pode abranger quantas linhas forem necessárias
   até que seja fechado com */
int numero = 10;
```

Além desses dois tipos de comentários comuns, o C# suporta ainda um terceiro tipo, especialmente útil para a geração de documentação:

3. **Comentários de documentação XML**: Começam com `///` ou `/** ... */`. Esses comentários são usados para documentar definições de classes, métodos, propriedades e outros membros da classe. Eles podem ser processados por ferramentas como o `docfx` ou o próprio Visual Studio para gerar uma documentação em HTML ou outro formato legível. Por exemplo:

```csharp
/// <summary>
/// A descrição do método MinhaFuncao.
/// </summary>
/// <param name="parametro">Descrição do parâmetro.</param>
/// <returns>Descrição do valor de retorno.</returns>
public int MinhaFuncao(int parametro)
{
    return parametro + 1;
}
```

---
### O que são tipos primitivos?
Os tipos primitivos em programação são os blocos de construção básicos dos dados, que representam os tipos mais simples e fundamentais de dados com os quais as linguagens de programação podem trabalhar. Eles são chamados de "primitivos" porque oferecem a forma mais básica de armazenamento de dados e são suportados diretamente pelo hardware do computador.

Na plataforma .NET, esses tipos são definidos pelo Common Language Runtime (CLR), que é o componente responsável pela execução de código e pela provisão de serviços básicos para as linguagens que o .NET suporta. Os tipos primitivos no .NET são também chamados de "tipos de valor", pois armazenam diretamente os dados na memória alocada na pilha, e não referências a objetos na heap.

Aqui estão alguns dos tipos primitivos em C#:

- `int`: Representa um inteiro de 32 bits e pode conter valores entre -2,147,483,648 e 2,147,483,647.
- `long`: Representa um inteiro de 64 bits e pode conter valores muito maiores, entre -9,223,372,036,854,775,808 e 9,223,372,036,854,775,807.
- `float`: Representa um número de ponto flutuante de precisão simples de 32 bits.
- `double`: Representa um número de ponto flutuante de precisão dupla de 64 bits.
- `bool`: Representa um valor booleano que pode ser `true` ou `false`.
- `char`: Representa um único caractere Unicode de 16 bits.
- `byte`: Representa um inteiro sem sinal de 8 bits, com valores de 0 a 255.
- `sbyte`: Representa um inteiro com sinal de 8 bits, com valores de -128 a 127.
- `short`: Representa um inteiro com sinal de 16 bits, com valores de -32,768 a 32,767.
- `ushort`: Representa um inteiro sem sinal de 16 bits, com valores de 0 a 65,535.
- `uint`: Representa um inteiro sem sinal de 32 bits, com valores de 0 a 4,294,967,295.
- `ulong`: Representa um inteiro sem sinal de 64 bits, com valores de 0 a 18,446,744,073,709,551,615.
- `decimal`: Representa um número decimal de 128 bits, com uma alta precisão adequada para cálculos financeiros e monetários.

Os tipos primitivos são definidos no namespace `System` do .NET e, portanto, estão sempre disponíveis para uso nos programas sem a necessidade de incluir um namespace adicional.

Esses tipos possuem métodos e propriedades embutidos, apesar de serem considerados primitivos, pois no .NET, até mesmo os tipos primitivos são tratados como objetos. Por exemplo, o tipo `int` no .NET tem métodos como `ToString()`, `CompareTo()`, `Equals()`, entre outros, porque na realidade ele é um alias para a estrutura `System.Int32`, que herda de `System.ValueType` e, indiretamente, de `System.Object`.

---
### Qual tipo base no .NET?
No .NET, o tipo base fundamental de todos os outros tipos é `System.Object`, frequentemente referido apenas como `object`. Este tipo reside no espaço de nomes `System`, que é o núcleo do .NET Framework Class Library (FCL). Todos os tipos em .NET, seja tipos de valor (value types) ou tipos de referência (reference types), derivam direta ou indiretamente de `System.Object`.

Aqui estão algumas das razões pelas quais `System.Object` é tão central para o .NET:

1. **Polimorfismo Base**: Como todos os tipos derivam de `System.Object`, qualquer variável do tipo `object` pode armazenar uma instância de qualquer tipo no .NET, o que permite um alto grau de polimorfismo. Isto é útil para coleções não genéricas, como `ArrayList`, que podem armazenar qualquer tipo de objeto.

2. **Métodos Comuns**: `System.Object` define um conjunto de métodos que estão disponíveis em todos os tipos, garantindo assim uma interface comum. Estes incluem:

   - `Equals(Object)`: Fornece uma maneira de verificar se dois objetos são iguais.
   - `GetHashCode()`: Retorna um código hash para o objeto, que é usado em estruturas de dados como tabelas de hash.
   - `GetType()`: Retorna o `System.Type` do objeto, que contém informações sobre o tipo do objeto em tempo de execução.
   - `ToString()`: Retorna uma representação de string do objeto, que é frequentemente sobrescrita em classes derivadas para fornecer uma representação mais significativa.

3. **Conversões de Tipo**: As conversões de tipo para o tipo `object` são implícitas para todos os tipos, o que significa que você pode atribuir qualquer valor ou objeto a uma variável do tipo `object` sem a necessidade de uma conversão explícita. Isso é conhecido como "boxing" quando se trata de tipos de valor, e é apenas uma referência direta para tipos de referência.

4. **Boxing e Unboxing**: Em .NET, você pode armazenar tipos de valor em variáveis do tipo `object`. Isso é chamado de "boxing". A operação oposta, chamada "unboxing", extrai o tipo de valor de dentro do objeto. Essas operações permitem que tipos de valor sejam tratados como objetos, embora com uma penalidade de desempenho devido à necessidade de alocação de heap e à cópia de dados.

5. **Herança de Objeto**: Quando você cria uma nova classe em .NET, por padrão, ela herda de `System.Object` se outra classe base não for especificada. Isso significa que mesmo que você não declare explicitamente a herança de `object`, sua classe ainda terá todos os métodos definidos por `System.Object`.

O papel de `System.Object` é fundamental na garantia de que todas as entidades no .NET tenham um mínimo de funcionalidade comum e possam ser tratadas de maneira uniforme em muitos cenários de programação. Isso facilita a criação de sistemas extensíveis e interoperáveis na plataforma .NET.

---
### Dado um var de um número real, qual tipo seria o var?
---
### Dado um var de um número inteiro, qual tipo seria o var?
---
### Qual a diferença entre char e string?
---
### Qual valor padrão do tipo char?
---
### Qual a diferença entre var e object?
---
### O que são tipos nulos?
---
### O que são alias? Cite 3 exemplos
---
### O que são conversões implícitas?
---
### O que são conversões explícitas?
---
### Qual a diferença entre parse e Convert?
---
### O que são operadores aritméticos e quais temos no C#?
---
### O que são operadores de atribuição e quais temos no C#?
---
### O que são operadores de comparação e quais temos no C#?
---
### O que são operadores lógicos e quais temos no C#?
---
### Cite duas estruturas condicionais que temos no C#
---
### Cite duas estruturas de repetição que temos no C#
---
### Qual a diferença entre while e do/while?
---
### O que são heap e stack?
---
### O que são tipos de valor e tipos de referência?
---
### Onde são armazenados os tipos de valor?
---
### Onde são armazenados os tipos de referência?
---
### O que são Structs?
---
### O que são enumeradores?
---
### O que é um GUID?
---