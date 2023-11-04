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

#### `class`
A palavra-chave `class` é usada para declarar uma classe, que é uma das principais construções de programação orientada a objetos no C#. Uma classe é como um blueprint para criar objetos, que encapsulam dados e comportamento. Quando você declara uma classe, você está criando um novo tipo de dado que pode ser instanciado como objetos.

```csharp
public class Carro {
    public string Modelo;
    public void Acelerar() {
        // Método para acelerar o carro
    }
}
```

#### `interface`
A palavra-chave `interface` define uma interface em C#. Interfaces são contratos que definem um conjunto de métodos e propriedades que as classes ou estruturas que as implementam devem conter. Interfaces são importantes para criar código altamente modular e reutilizável e são uma parte central da programação orientada a objetos e do design de software.

```csharp
public interface IVeiculo {
    void Acelerar();
    void Frear();
}
```

#### `void`
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
Quando você utiliza a palavra-chave `var` para declarar uma variável com um número real literal, o tipo atribuído depende da notação do número real fornecido.

Por exemplo:

```csharp
var number = 1.0;
```

Neste caso, sem qualquer sufixo adicional, o tipo inferido seria `double`. 

Outros tipos de números reais em .NET incluem `float` e `decimal`. Se você quiser que o número seja interpretado como um `float` ou um `decimal`, você deve usar os sufixos `f` ou `m`, respectivamente:

```csharp
var number = 1.0f; // Inferido como float
var number = 1.0m; // Inferido como decimal
```

Portanto, ao usar `var`, o tipo será determinado automaticamente pelo compilador com base no literal fornecido, a menos que você especifique um sufixo que força o compilador a tratar o literal como um tipo específico de ponto flutuante.

---
### Dado um var de um número inteiro, qual tipo seria o var?
Quando você utiliza a palavra-chave `var` para declarar uma variável, você está indicando ao compilador que ele deve inferir o tipo da variável com base no valor que é atribuído a ela no momento da declaração. Isso é conhecido como inferência de tipo local e é uma característica da linguagem C# que foi introduzida na versão 3.0.

Se você declara uma variável com `var` e a inicializa com um número inteiro, como mostrado no exemplo abaixo:

```csharp
var numero = 10;
```

O compilador do C# irá inferir que o tipo da variável `numero` é `int`, que é o tipo padrão para números inteiros literais em C# sem um sufixo que indique outro tipo de inteiro (como `long`, `uint`, etc.).

Aqui está como a inferência de tipo funciona nesse caso:

1. O compilador vê o valor literal `10`, que se ajusta dentro do intervalo de um `int` (que em C# é um inteiro de 32 bits com sinal).
2. Não há nenhum sufixo no literal que sugeriria que o valor deve ser tratado como um tipo diferente de inteiro (como `L` para `long` ou `U` para `unsigned int`).
3. O compilador então infere que o tipo da variável `numero` é `int`.

Isso significa que, após essa linha de código, você só pode usar a variável `numero` para armazenar valores que são compatíveis com o tipo `int`. Tentar atribuir um valor que não é compatível, como uma string ou um número decimal, resultará em um erro de compilação.

---
### Qual a diferença entre char e string?
No contexto da plataforma .NET, `char` e `string` são tipos de dados que são usados para representar caracteres e sequências de caracteres, respectivamente. Aqui estão as diferenças principais entre eles:

#### `char`

- `char` representa um único caractere Unicode de 16 bits.
- É um tipo de valor (`ValueType`) e, portanto, é armazenado na pilha.
- `char` é uma abstração do .NET para o tipo de dados primitivo `System.Char`.
- Pode conter qualquer valor Unicode de `\u0000` a `\uffff`.
- Não é possível para um `char` ser `null`, mas ele pode ser o caractere nulo (`\0`).
- É utilizado quando você está trabalhando com um único caractere, como em operações de controle de caracteres, conversões de dígitos para caracteres, etc.

Exemplo de declaração e uso de `char`:

```csharp
char letra = 'A'; // representação de um único caractere
```

#### `string`

- `string` representa uma sequência de caracteres Unicode de 16 bits.
- É um tipo de referência (`ReferenceType`) e, portanto, é armazenado no heap, embora tenha algumas otimizações especiais em .NET como a interning de strings.
- `string` é uma abstração do .NET para o tipo de dados primitivo `System.String`.
- Pode ser composta de zero ou mais caracteres Unicode e pode ser considerada como um array de `char`.
- Uma `string` pode ser `null` ou vazia (`""`), o que não é o mesmo que um `char` nulo.
- É usada quando você está trabalhando com texto, como em manipulação de texto, armazenamento de dados textuais, entre outros.

Exemplo de declaração e uso de `string`:

```csharp
string palavra = "Olá Mundo!"; // representação de uma sequência de caracteres
```

Em resumo, use `char` quando estiver lidando com um único caractere e `string` quando estiver trabalhando com textos compostos por múltiplos caracteres.

---
### Qual valor padrão do tipo char?
O tipo `char` é um tipo de valor que representa um caractere Unicode de 16 bits. De acordo com a especificação da linguagem C#, o valor padrão para tipos de valor, como o `char`, é o zero-bit pattern, que resulta em `\0` para o tipo `char`.

Portanto, o valor padrão do tipo `char` é o caractere Unicode `U+0000`, que é o "null character" ou "caractere nulo". Este não deve ser confundido com o valor `null` que é usado para tipos de referência, indicando a ausência de uma instância de objeto. O "null character" é um valor válido dentro do conjunto de caracteres Unicode, mas geralmente é usado em programação para indicar o fim de uma string em linguagens de programação de baixo nível como C e C++.

Aqui está um exemplo de como isso pode ser representado em C#:

```csharp
char defaultChar = default(char); // defaultChar será '\0'
```

O `default(char)` irá produzir `\0`, que é o valor padrão para o tipo `char`.

---
### Qual a diferença entre var e object?

A diferença entre `var` e `object` é fundamental para entender como a linguagem C# lida com tipos de dados.

#### `object`

- **Definição**: `object` é a classe base para todos os tipos de dados em .NET. Isso significa que qualquer tipo pode ser convertido implicitamente para `object`.
- **Tipagem**: Ao declarar uma variável como `object`, você está utilizando tipagem estática e explícita. Você está dizendo explicitamente que a variável é do tipo `object`.
- **Boxing e Unboxing**: Quando você atribui um tipo de valor (como um `int`, `bool`, etc.) a uma variável do tipo `object`, ocorre um processo chamado "boxing", onde o valor é encapsulado dentro de um objeto no heap. O inverso, "unboxing", extrai o valor de volta a um tipo de valor, e deve ser feito de maneira explícita.
- **Performance**: Devido ao boxing e unboxing, usar `object` pode ter implicações na performance, principalmente se houver muitas conversões de tipos de valor para referência e vice-versa.
- **Flexibilidade**: `object` pode ser usado para armazenar qualquer tipo de dado, o que o torna muito flexível, mas ao custo de segurança de tipo e performance.
- **Exemplo de Uso**:
  ```csharp
  object obj = 10; // Boxing do valor 10.
  int num = (int)obj; // Unboxing e conversão explícita de volta para int.
  ```

#### `var`

- **Definição**: `var` é uma palavra-chave introduzida no C# 3.0 que permite a declaração implícita de tipo de variáveis. O compilador infere o tipo da variável pelo valor que lhe é atribuído no momento da sua inicialização.
- **Tipagem**: Ao usar `var`, você está utilizando tipagem estática, mas implícita. O tipo da variável é determinado no tempo de compilação e não pode mudar depois disso, mas você não precisa especificar o tipo explicitamente.
- **Performance**: Como o tipo de uma variável declarada com `var` é definido em tempo de compilação e não envolve boxing ou unboxing (a menos que atribua explicitamente a um tipo `object`), ela tem a mesma performance que uma variável tipada explicitamente.
- **Legibilidade e Manutenção**: `var` pode tornar o código mais legível, especialmente quando lidando com tipos complexos, mas se usado excessivamente pode tornar o código menos claro em relação ao tipo de dados que a variável representa.
- **Exemplo de Uso**:
  ```csharp
  var num = 10; // O compilador inferirá que num é do tipo int.
  ```
  
#### Considerações Importantes

- `var` só pode ser usado quando uma variável é inicializada. Você não pode declarar uma variável `var` sem inicializá-la.
- `var` não significa "variant" e não está relacionado com a tipagem dinâmica. Uma vez que o tipo é inferido, ele é fixo e o compilador tratará a variável como sendo daquele tipo específico.
- `var` não é uma palavra-chave que indica "qualquer tipo"; ela simplesmente diz para o compilador "veja o que estou atribuindo a essa variável e inferir o tipo a partir disso".
- O uso de `var` e `object` depende do contexto e da necessidade. Se precisar de uma variável que possa armazenar diferentes tipos de dados durante seu ciclo de vida, você precisará usar `dynamic` ou `object`. Se souber que o tipo de dados não vai mudar e quiser simplicidade e clareza, o `var` é a escolha adequada.

Em resumo, `var` é sobre deixar o compilador decidir o tipo baseado na atribuição inicial, mantendo tipagem estática e performance otimizada. `object`, por outro lado, é sobre a flexibilidade de armazenar qualquer tipo de dados em uma variável, mas com possíveis implicações na performance devido ao boxing e unboxing.

---
### O que são tipos nulos?

Tipos nulos são uma maneira de representar a ausência de valor para tipos de dados que normalmente requerem um valor. Tipos de valor, como `int`, `float`, `DateTime`, não podem ser nulos por padrão. Eles sempre devem conter um valor, o que significa que, se você declarar uma variável desse tipo e não inicializá-la, ela automaticamente terá um valor padrão (por exemplo, `0` para números inteiros, `false` para `bool`, etc.).

No entanto, há situações em que é útil ter a capacidade de representar que uma variável não tem nenhum valor atribuído, como quando você está trabalhando com bancos de dados ou outras operações onde um valor pode ser desconhecido ou inaplicável. Para lidar com essas situações, .NET fornece os chamados tipos anuláveis ou nulos (nullable types).

Um tipo anulável é criado usando o símbolo `?` após o tipo de valor. Por exemplo, `int?` é um tipo anulável de `int`. Isso significa que além dos valores normais de `int`, ele também pode conter `null`, o que indica a ausência de valor.

Exemplo de declaração de um tipo anulável:

```csharp
int? numeroAnulavel = null;
```

Neste exemplo, `numeroAnulavel` é uma variável que pode conter qualquer valor `int` ou `null`.

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