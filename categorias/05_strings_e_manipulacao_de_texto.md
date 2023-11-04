# Strings e Manipulação de Texto

Este arquivo foca em questões sobre operações e manipulações de strings em C#.

## Perguntas e Respostas

### O que é interpolação de String?

A interpolação de string é uma forma de construir strings em C# que torna mais fácil a incorporação de valores de variáveis dentro de uma string literal. A interpolação de string é feita utilizando-se o símbolo `$` antes da string literal e inserindo as variáveis ou expressões entre chaves `{}` dentro da string. Isso facilita a leitura e manutenção do código ao eliminar a necessidade de usar a concatenação de strings ou métodos como `String.Format`.

Exemplo de interpolação de string:

```csharp
string nome = "Maria";
int idade = 30;
string mensagem = $"Olá, {nome}! Você tem {idade} anos.";
Console.WriteLine(mensagem);
```

No exemplo acima, o valor das variáveis `nome` e `idade` são inseridos na string `mensagem` nos locais correspondentes.

---
### Qual a finalidade do método CompareTo?

O método `CompareTo` é usado para comparar duas strings e determinar a ordem alfabética relativa das mesmas. Ele é um método da interface `IComparable` e retorna um inteiro que indica a relação entre as strings comparadas:

- Um valor negativo: se a string que invoca o método vem antes da string passada como parâmetro na ordem alfabética.
- Zero: se as duas strings são equivalentes na ordem de classificação.
- Um valor positivo: se a string que invoca o método vem depois da string passada como parâmetro na ordem alfabética.

Exemplo:

```csharp
string str1 = "apple";
string str2 = "banana";
int comparison = str1.CompareTo(str2);
// comparison terá um valor negativo, porque "apple" vem antes de "banana".
```

---
### Qual a finalidade do método Contains?

O método `Contains` é utilizado para verificar se uma string contém uma subsequência de caracteres específica. O método retorna `true` se a subsequência estiver presente na string e `false` se não estiver.

Exemplo:

```csharp
string frase = "Olá, mundo!";
bool contem = frase.Contains("mundo"); // retorna true
```

---
### Qual a finalidade do método StartsWith e EndsWith?

- `StartsWith`: Este método é usado para verificar se uma string começa com uma subsequência de caracteres específica. Ele retorna `true` se a string iniciar com a subsequência desejada.

Exemplo:

```csharp
string frase = "Bom dia!";
bool comecaCom = frase.StartsWith("Bom"); // retorna true
```

- `EndsWith`: Similar ao `StartsWith`, porém verifica se uma string termina com uma subsequência de caracteres específica. Ele retorna `true` se a string terminar com a subsequência desejada.

Exemplo:

```csharp
string frase = "Boa noite!";
bool terminaCom = frase.EndsWith("noite!"); // retorna true
```

---
### Qual a finalidade do método Equals?

O método `Equals` é utilizado para comparar duas instâncias de um tipo de dado (tipos de valor ou de referência) e determinar se são iguais. Para tipos de valor, compara os valores em si, enquanto para tipos de referência, por padrão, compara os endereços de memória, a menos que o método seja sobrescrito para comparar os estados dos objetos.

Aqui está um exemplo simples:

```csharp
string a = "hello";
string b = "hello";

bool areEqual = a.Equals(b); // Retorna true, pois o conteúdo das strings é o mesmo.
```

Se você estiver implementando sua própria classe e desejar que o método `Equals` verifique a igualdade com base nos dados da classe, você precisará sobrescrever o método e implementar sua própria lógica de comparação.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    public override bool Equals(Object obj)
    {
        // Se o objeto passado não é uma instância de Person, retorne false.
        if (obj == null || !(obj is Person))
            return false;

        // Se é uma instância de Person, compare os valores dos campos.
        Person other = (Person)obj;
        return this.Name == other.Name && this.Age == other.Age;
    }

    // É uma boa prática também sobrescrever o método GetHashCode
    // quando o Equals é sobrescrito.
    public override int GetHashCode()
    {
        return HashCode.Combine(Name, Age);
    }
}
```

O `Equals` é útil quando você precisa de uma comparação de igualdade personalizada ou quando quer verificar se duas variáveis se referem ao mesmo objeto na memória (quando não sobrescrito).

---

### Qual a finalidade do método IndexOf e LastIndexOf?

#### `IndexOf`

O método `IndexOf` em C# é utilizado para determinar a posição de um caractere ou uma substring dentro de outra string. Ele retorna o índice baseado em zero da primeira ocorrência da string ou caractere procurado. Se o caractere ou a substring não for encontrado, `IndexOf` retorna -1. Este método é frequentemente utilizado para encontrar a posição de um determinado conjunto de caracteres em uma string antes de realizar operações como inserção, substituição ou remoção.

Por exemplo:

```csharp
string sample = "Hello, World!";
int index = sample.IndexOf('W'); // Retorna 7, que é a posição do 'W' em "World"
```

#### `LastIndexOf`

O método `LastIndexOf` funciona de maneira semelhante ao `IndexOf`, mas, em vez de retornar a primeira ocorrência de um caractere ou substring, ele retorna a última ocorrência dentro da string. Isso é especialmente útil quando você precisa encontrar uma ocorrência de um caractere ou substring a partir do final de uma string.

Por exemplo:

```csharp
string sample = "Hello, World! Welcome to the World!";
int lastIndex = sample.LastIndexOf("World"); // Retorna 28, a posição da segunda ocorrência de "World"
```

### Qual a finalidade do método ToLower e ToUpper?

Estes dois métodos são usados para alterar a capitalização dos caracteres em uma string.

- `ToLower`: Converte todos os caracteres alfabéticos em uma string para minúsculas. Isso é útil para tarefas como normalizar strings para comparações que não diferenciam maiúsculas de minúsculas.

```csharp
string sample = "Hello, World!";
string lowercased = sample.ToLower(); // Retorna "hello, world!"
```

- `ToUpper`: Converte todos os caracteres alfabéticos em uma string para maiúsculas. Pode ser utilizado para apresentar strings em formatos padronizados, como códigos ou identificadores que são tradicionalmente em maiúsculas.

```csharp
string sample = "Hello, World!";
string uppercased = sample.ToUpper(); // Retorna "HELLO, WORLD!"
```

---
### Qual a finalidade do método Insert?

Permite inserir uma string dentro de outra string em uma posição especificada. A posição é indicada por um índice baseado em zero. O método retorna uma nova string com o conteúdo inserido, já que as strings em C# são imutáveis e qualquer operação que pareça modificar uma string na verdade retorna uma nova string com as alterações desejadas.

Aqui está a assinatura do método `Insert`:

```csharp
public string Insert(int startIndex, string value);
```

- `startIndex`: A posição na string original onde a nova string deve ser inserida.
- `value`: A string a ser inserida.

Exemplo de uso:

```csharp
string original = "Hello World!";
string toInsert = "C# ";
// Insere "C# " na posição 6 de "Hello World!".
string modified = original.Insert(6, toInsert); // "Hello C# World!"
```

No exemplo acima, a string `"C# "` é inserida na posição 6 da string original `"Hello World!"`, resultando em `"Hello C# World!"`. Note que `original` permanece inalterado após a operação; `modified` contém a nova string resultante.

O método `Insert` é útil em situações onde você precisa adicionar caracteres ou palavras em pontos específicos de uma string, como na construção de uma string formatada a partir de várias partes ou na manipulação de texto onde certos valores devem ser inseridos em posições específicas.

---
### Qual a finalidade do método Length?

Retorna o número de caracteres na string. Como as strings são arrays de caracteres, `Length` fornece a contagem total de elementos no array, que corresponde ao número de caracteres Unicode na string.

Aqui está como você pode usar a propriedade `Length`:

```csharp
string example = "Hello, World!";
int lengthOfString = example.Length; // Retorna 13
```

No exemplo acima, `lengthOfString` seria 13, porque a string `"Hello, World!"` contém 13 caracteres, incluindo a vírgula e o espaço.

`Length` é útil sempre que você precisa saber quantos caracteres existem em uma string, o que é comum em muitos cenários como:

- Validação de entrada: para garantir que uma string atenda a um requisito de comprimento específico.
- Processamento de texto: para iterar sobre todos os caracteres de uma string.
- Corte de strings: para determinar se é necessário truncar uma string para um certo tamanho.

É importante notar que `Length` retorna o número de unidades de código UTF-16 na string e não necessariamente o número exato de caracteres Unicode, pois alguns caracteres Unicode são representados por duas unidades de código (conhecidos como pares substitutos).

---
### Qual a finalidade do método Remove?
Usado para excluir uma parte de uma string, começando em uma posição especificada e, opcionalmente, por um determinado número de caracteres. A classe `String` possui sobrecargas do método `Remove` que permitem especificar apenas o índice inicial ou o índice inicial junto com o número de caracteres a serem removidos. Como as strings em C# são imutáveis, esse método não altera a string original, mas retorna uma nova string com a remoção aplicada.

Aqui estão as duas sobrecargas do método `Remove`:

1. `Remove(int startIndex)`: Remove todos os caracteres da posição `startIndex` até o final da string.
2. `Remove(int startIndex, int count)`: Remove `count` caracteres começando na posição `startIndex`.

Exemplos de Uso:

1. **Removendo caracteres do índice até o final:**

```csharp
string original = "Hello, World!";
string result = original.Remove(5); // Remove a partir do índice 5 até o fim da string.
Console.WriteLine(result); // Saída: "Hello"
```

2. **Removendo uma quantidade específica de caracteres:**

```csharp
string original = "Hello, World!";
string result = original.Remove(7, 5); // Remove 5 caracteres a partir do índice 7.
Console.WriteLine(result); // Saída: "Hello, !"
```

O método `Remove` é particularmente útil para situações em que você precisa limpar ou extrair determinadas partes de uma string, como ao manipular caminhos de arquivos, entrada de usuário ou ao processar dados de texto que requerem tratamento especial para certas subcadeias.

---
### Qual a finalidade do método Replace?
Usado para substituir todas as ocorrências de uma substring especificada dentro de uma string por outra substring. Esse método é muito útil para realizar operações de substituição de texto, como formatar dados, corrigir erros de digitação ou atualizar partes de uma string dinamicamente.

Existem principalmente duas versões do método `Replace`:

1. `Replace(char oldChar, char newChar)`: Substitui todas as ocorrências do caractere especificado `oldChar` pelo caractere `newChar`.

2. `Replace(string oldValue, string newValue)`: Substitui todas as ocorrências da string especificada `oldValue` pela string `newValue`.

Assim como outros métodos da classe `String`, `Replace` retorna uma nova string com as substituições aplicadas, uma vez que as strings em C# são imutáveis e não podem ser alteradas após serem criadas.

Exemplos de Uso:

1. **Substituição de Caracteres:**

```csharp
string original = "Hello, World!";
string result = original.Replace('l', '7');
Console.WriteLine(result); // Saída: "He77o, Wor7d!"
```

Neste exemplo, todas as ocorrências do caractere `'l'` são substituídas pelo caractere `'7'`.

2. **Substituição de Substrings:**

```csharp
string original = "Hello, World!";
string result = original.Replace("World", "Universe");
Console.WriteLine(result); // Saída: "Hello, Universe!"
```

Neste exemplo, a substring `"World"` é substituída pela substring `"Universe"`.

O método `Replace` é amplamente utilizado em cenários que vão desde a limpeza de dados de entrada até a manipulação de strings para a geração de saídas formatadas, como a criação de templates de texto onde placeholders são substituídos por valores dinâmicos.

---
### Qual a finalidade do método Split?
Utilizado para dividir uma string em um array de substrings com base em delimitadores que são especificados como argumentos do método. É uma ferramenta essencial quando se trata de processamento de texto, pois permite desmembrar uma cadeia de caracteres em partes menores para análise ou processamento adicional.

A classe `String` oferece várias sobrecargas do método `Split`. Algumas das mais comuns permitem especificar:

- Um único caractere como delimitador.
- Um array de caracteres contendo vários delimitadores.
- Um array de strings contendo vários delimitadores.
- Opções para controlar como as substrings vazias são manipuladas (por exemplo, excluí-las do array resultante).

O método `Split` não altera a string original; em vez disso, ele retorna um novo array de strings.

Exemplos de Uso:

1. **Usando um Caractere como Delimitador:**

```csharp
string data = "apple,banana,cherry";
string[] fruits = data.Split(',');
foreach (var fruit in fruits)
{
    Console.WriteLine(fruit);
}
// Saída:
// apple
// banana
// cherry
```

2. **Usando Múltiplos Caracteres como Delimitadores:**

```csharp
string data = "apple;banana|cherry";
char[] delimiters = new char[] { ';', '|' };
string[] fruits = data.Split(delimiters);
foreach (var fruit in fruits)
{
    Console.WriteLine(fruit);
}
// Saída:
// apple
// banana
// cherry
```

3. **Excluindo Substrings Vazias do Resultado:**

```csharp
string data = "apple,,banana,cherry,";
string[] fruits = data.Split(new char[] { ',' }, StringSplitOptions.RemoveEmptyEntries);
foreach (var fruit in fruits)
{
    Console.WriteLine(fruit);
}
// Saída:
// apple
// banana
// cherry
```
O método `Split` é comumente usado para processar dados de arquivos CSV, realizar análise de logs, quebrar linhas de texto em palavras ou frases, e em muitas outras situações onde se deseja extrair informações específicas de uma string mais extensa.

---
### Qual a finalidade do método Substring?
Usado para extrair uma substring de uma string maior. Este método permite especificar o ponto de início da substring e, opcionalmente, quantos caracteres devem ser incluídos na substring extraída.

A classe `String` fornece duas sobrecargas do método `Substring`:

1. `Substring(int startIndex)`: Retorna uma nova string que é uma substring da string original, começando no índice especificado até o final da string original.

2. `Substring(int startIndex, int length)`: Retorna uma nova string que é uma substring da string original, começando no índice especificado e com o número de caracteres especificado.

Exemplos de Uso:

1. **Extraindo até o Final da String:**

```csharp
string text = "Hello, World!";
string sub = text.Substring(7); // Começa no índice 7 e vai até o final.
Console.WriteLine(sub); // Saída: "World!"
```

Neste exemplo, a substring `"World!"` é extraída começando do índice 7 da string original até o final da mesma.

2. **Extraindo um Número Específico de Caracteres:**

```csharp
string text = "Hello, World!";
string sub = text.Substring(7, 5); // Começa no índice 7 e pega 5 caracteres.
Console.WriteLine(sub); // Saída: "World"
```

Neste exemplo, exatamente 5 caracteres são extraídos começando do índice 7, resultando na substring `"World"`.

O método `Substring` é particularmente útil para tarefas de processamento de texto onde você precisa isolar partes específicas de uma string, como ao processar identificadores, códigos ou ao trabalhar com formatos de texto que têm estruturas de dados fixas.

---
### Qual a finalidade do método Trim?

Usado para remover todos os espaços em branco iniciais e finais de uma string, incluindo espaços, tabs, e outros caracteres de espaço em branco Unicode. Este método é útil para limpar dados de entrada do usuário, processar texto antes de armazenamento ou comparação, e sempre que é necessário remover espaços extras que podem causar problemas em operações de string ou em comparações de texto.

Existem também as variantes `TrimStart` e `TrimEnd`, que removem espaços em branco apenas do início ou apenas do fim da string, respectivamente.

Além disso, `Trim`, `TrimStart` e `TrimEnd` podem ser passados parâmetros que especificam um conjunto de caracteres a serem removidos em vez de apenas espaços em branco. Se nenhum parâmetro for fornecido, eles removerão os caracteres de espaço em branco padrão.

Exemplos de Uso:

1. **Removendo Espaços em Branco Padrão:**

```csharp
string text = "   Hello, World!   ";
string trimmed = text.Trim();
Console.WriteLine($"'{trimmed}'"); // Saída: 'Hello, World!'
```

Aqui, `Trim` remove todos os espaços do início e do fim da string original.

2. **Removendo Caracteres Específicos:**

```csharp
string text = "+++Hello, World!+++";
string trimmed = text.Trim('+');
Console.WriteLine($"'{trimmed}'"); // Saída: 'Hello, World!'
```

Neste exemplo, `Trim` é usado para remover todos os caracteres '+' do início e do fim da string.

O método `Trim` não altera a string original, pois strings em C# são imutáveis. Em vez disso, ele retorna uma nova string com os espaços em branco (ou outros caracteres especificados) removidos. Este comportamento é consistente com outros métodos de manipulação de strings no .NET, onde a string original permanece inalterada e um novo objeto string é retornado com as modificações aplicadas.

---
### O que é StringBuilder e quando devemos utilizar?

`StringBuilder` é uma classe no .NET Framework localizada no namespace `System.Text` que é usada para manipular sequências de caracteres de forma mais eficiente do que usando uma instância da classe `String`. Isso se deve ao fato de que objetos `String` são imutáveis, o que significa que qualquer alteração em um objeto `String` existente resulta na criação de um novo objeto `String`. Em contraste, `StringBuilder` pode ser modificado sem criar uma nova instância a cada vez, o que o torna ideal para cenários onde são necessárias muitas manipulações de strings.

### Quando usar `StringBuilder`:
- **Modificações Frequentes**: Use `StringBuilder` quando você espera fazer um número significativo de alterações na string, como em loops ou quando concatenando muitos fragmentos de string.
  
- **Grande Quantidade de Dados**: É útil quando se trabalha com grandes volumes de texto que precisam ser construídos ou modificados dinamicamente.

- **Performance**: Em situações onde a performance é uma consideração importante e a manipulação de strings está se mostrando um gargalo, substituir `String` por `StringBuilder` pode resultar em melhorias significativas.

Exemplo de Uso do `StringBuilder`:

```csharp
StringBuilder sb = new StringBuilder();
sb.Append("The quick brown fox ");
sb.AppendLine("jumps over the lazy dog.");
sb.AppendFormat("The time is now {0}", DateTime.Now);

// Modificações são feitas no mesmo objeto, sem criar novos
for (int i = 0; i < 10; i++)
{
    sb.AppendLine("Adding another line.");
}

// Convertendo o StringBuilder de volta para uma string regular quando terminado
string result = sb.ToString();
Console.WriteLine(result);
```

Neste exemplo, várias operações são realizadas no `StringBuilder` sem a necessidade de criar novas instâncias de strings, o que seria o caso se estivéssemos usando concatenação de strings com objetos `String`.

Apesar da eficiência do `StringBuilder` em termos de performance para certos cenários, ele pode ser uma opção excessiva quando você tem apenas algumas concatenações simples. Para pequenas operações ou concatenações que são compiladas em tempo de compilação ou ocorrem poucas vezes em tempo de execução, o uso da classe `String` é mais direto e pode ser igualmente eficiente.

---
### O que é Regex e quando devemos utilizar?

`Regex` é uma abreviação de Regular Expression, que é uma poderosa ferramenta para busca, substituição e manipulação de texto baseada em padrões definidos. Em C#, a funcionalidade de expressões regulares é fornecida pelo namespace `System.Text.RegularExpressions`.

Expressões regulares são uma linguagem de padrões que oferece uma forma flexível e eficiente de analisar strings. Você pode definir padrões complexos de caracteres que ajudam a identificar se partes de uma string correspondem a um formato específico, a extrair valores de uma string ou a realizar operações complexas de busca e substituição.

#### Quando usar Regex:
- **Validação de Formatos**: Quando você precisa validar formatos complexos como emails, URLs, códigos postais, números de telefone, etc.
- **Análise e Extração de Dados**: Para extrair informações específicas de textos, como capturar datas, números ou substrings que seguem um padrão específico.
- **Operações de Busca Avançada**: Quando `String.Contains`, `String.StartsWith`, `String.EndsWith` e métodos similares não são suficientes para suas necessidades de busca.
- **Substituições Complexas de Texto**: Quando você precisa substituir partes de uma string que correspondem a um padrão complexo, por exemplo, transformar datas de um formato para outro.
- **Divisão de Strings**: Quando `String.Split` não é suficiente porque você precisa dividir uma string baseada em um padrão mais complexo do que um simples delimitador.

Exemplo de Uso do `Regex`:

```csharp
using System;
using System.Text.RegularExpressions;

class Program
{
    static void Main()
    {
        string input = "The quick brown fox jumps over 13 lazy dogs.";
        string pattern = @"\b\w+ow\b"; // Palavras que terminam com "ow"

        // Encontrando todas as correspondências
        MatchCollection matches = Regex.Matches(input, pattern);
        foreach (Match match in matches)
        {
            Console.WriteLine("Found '{0}' at position {1}", match.Value, match.Index);
        }

        // Substituindo texto
        string replaced = Regex.Replace(input, @"\d+", "#");
        Console.WriteLine(replaced);

        // Validando um padrão (neste caso, números)
        string patternForDigits = @"^\d+$";
        bool isNumber = Regex.IsMatch("12345", patternForDigits);
        Console.WriteLine("String contains only digits: " + isNumber);
    }
}
```

**Output:**
```
Found 'brown' at position 10
The quick brown fox jumps over # lazy dogs.
String contains only digits: True
```

Cada vez que você considerar o uso de `Regex`, é importante ponderar a complexidade e a performance. Expressões regulares podem ser menos eficientes do que outras operações de string se mal utilizadas, e elas podem ser difíceis de manter e entender se forem muito complexas. Portanto, use-as quando as alternativas mais simples não atenderem às suas necessidades ou quando a clareza e eficiência do seu código puderem se beneficiar de sua expressividade e potência.

---