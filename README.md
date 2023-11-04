# Repositório de Perguntas e Respostas sobre .NET
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Este repositório contém uma coleção de perguntas e respostas voltadas para a linguagem C# e a plataforma .NET. É um recurso útil para aqueles que estão se preparando para entrevistas de emprego, estudando para certificações ou simplesmente buscando aprimorar seus conhecimentos no .NET Framework, .NET Core e .NET 5/6.

As perguntas foram originadas de um artigo criado por [André Baltieri](https://balta.io), também conhecido como Balta, e podem ser acessadas no seguinte link: [Perguntas para entrevistas de C#](https://balta.io/blog/perguntas-entrevista-csharp).

## Categorias

As perguntas estão organizadas por tópicos para facilitar o acesso e o estudo:

### [Fundamentos e Conceitos Básicos](categorias/01_fundamentos_e_conceitos_basicos.md)
Questões sobre os princípios fundamentais do .NET e os conceitos básicos de C#.

- [x] [O C# é uma linguagem compilada, tipada e gerenciada, o que isto significa?](categorias/01_fundamentos_e_conceitos_basicos.md/#o-c-é-uma-linguagem-compilada-tipada-e-gerenciada-o-que-isto-significa)
- O que diferencia uma linguagem compilada de uma interpretada?
- Explique como o C# funciona
- O que é o CLR?
- O que é IL?
- O que é um Framework?
- O que é o .NET?
- O que é o .NET Standard?
- O que significa LTS na versão do software?
- O que é um Runtime?
- O que é um SDK?
- O que é um CLI?
- O que é uma Solution?
- Explique o que é versão semântica?

### [Estrutura de Projetos e Soluções](categorias/02_estrutura_de_projetos_e_solucoes.md)
Detalhes sobre como projetos e soluções são estruturados em um ambiente .NET.

- Cite 3 tipos de projetos que temos no .NET
- Qual nome do método principal de um Console App?
- Qual a finalidade da pasta Properties?
- Qual a finalidade das pastas Bin e Obj?
- O que são Namespaces?

### [Programação Básica em C#](categorias/03_programacao_basica_csharp.md)
Perguntas que cobrem a sintaxe básica e as construções da linguagem C#.

- Quais partes compõe um programa em C#?
- Qual a finalidade do Using?
- Qual a diferença entre uma variável e uma constante?
- Cite 3 nomes reservados que temos no C#
- Quais formas temos de comentar código em C#?
- O que são tipos primitivos?
- Qual tipo base no .NET?
- Dado um var de um número real, qual tipo seria o var?
- Dado um var de um número inteiro, qual tipo seria o var?
- Qual a diferença entre char e string?
- Qual valor padrão do tipo char?
- Qual a diferença entre var e object?
- O que são tipos nulos?
- O que são alias? Cite 3 exemplos
- O que são conversões implícitas?
- O que são conversões explícitas?
- Qual a diferença entre parse e Convert?
- O que são operadores aritméticos e quais temos no C#?
- O que são operadores de atribuição e quais temos no C#?
- O que são operadores de comparação e quais temos no C#?
- O que são operadores lógicos e quais temos no C#?
- Cite duas estruturas condicionais que temos no C#
- Cite duas estruturas de repetição que temos no C#
- Qual a diferença entre while e do/while?
- O que são heap e stack?
- O que são tipos de valor e tipos de referência?
- Onde são armazenados os tipos de valor?
- Onde são armazenados os tipos de referência?
- O que são Structs?
- O que são enumeradores?
- O que é um GUID?

### [Métodos e Parâmetros](categorias/04_metodos_e_parametros.md)
Explicações sobre a definição e utilização de métodos e a passagem de parâmetros em C#.

- Como definimos que um método não retorna valor algum?
- Podemos ter métodos sem parâmetros no C#?
- Como tornamos um parâmetro opcional no C#?

### [Strings e Manipulação de Texto](categorias/05_strings_e_manipulacao_de_texto.md)
Questões focadas na manipulação de strings e operações com texto no C#.

- O que é interpolação de String?
- Qual a finalidade do método CompareTo?
- Qual a finalidade do método Contains?
- Qual a finalidade do método StartsWith e EndsWith?
- Qual a finalidade do método Equals?
- Qual a finalidade do método IndexOf e LastIndexOf?
- Qual a finalidade do método ToLower e ToUpper?
- Qual a finalidade do método Insert?
- Qual a finalidade do método Length?
- Qual a finalidade do método Remove?
- Qual a finalidade do método Replace?
- Qual a finalidade do método Split?
- Qual a finalidade do método Substring?
- Qual a finalidade do método Trim?
- O que é StringBuilder e quando devemos utilizar?
- O que é Regex e quando devemos utilizar?

### [Data, Hora e Timezones](categorias/06_data_hora_e_timezones.md)
Como lidar com datas, horas e fusos horários em aplicações .NET.

- O que é o DateTime?
- Como obtemos a data de hoje no C#?
- Como convertemos uma data para String?
- Como comparamos duas datas em C#?
- Como podemos obter o ano, mês ou dia no C#?
- Como podemos obter o último dia do mês no C#?
- Podemos criar datas nulas?
- O que são nullable types?
- O que é Timezone?
- Como obtermos a data sem um Timezone no C#?
- O que é DateTime Offset?
- O que é um TimeSpan?
- Qual a finalidade do Math.Round, Math.Celling e Math.Floor?

### [Coleções, Listas e Generics](categorias/07_colecoes_listas_e_generics.md)
Exploração do uso de coleções, listas e tipos genéricos no C#.

- Qual a diferença entre IEnumerable, IList e ICollection?
- Qual a diferença entre List e IList?
- Qual a finalidade do método Add e AddRange em uma lista?
- Qual a finalidade do método Clear em uma lista?
- Qual a finalidade do método Contains em uma lista?
- Qual a finalidade do método CopyTo em uma lista?
- Qual a finalidade do método Exists em uma lista?
- Qual a finalidade do método Find e FindAll em uma lista?
- Qual a finalidade do método IndexOf e LastIndexOf em uma lista?
- Qual a finalidade do método FindIndex, FindLast e FindLastIndex em uma lista?
- Qual a finalidade do método Insert e InsertRange em uma lista?
- Qual a finalidade do método Remove, RemoveAll, RemoveAt e RemoveRange em uma lista?
- Qual a finalidade do método Reverse em uma lista?
- Qual a finalidade do método Sort em uma lista?
- Qual a finalidade do método ToArray em uma lista?
- Qual a finalidade do método TrueForAll em uma lista?
- Qual a finalidade do método ConvertAll em uma lista?
- Qual a finalidade do método ForEach em uma lista?
- Qual a finalidade do método Where em uma lista?
- Qual a finalidade do método First em uma lista?
- Qual a finalidade do método OrderBy em uma lista?
- Qual a finalidade do método Select em uma lista?

### [Orientação a Objetos e Conceitos Avançados](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md)
Questões aprofundadas sobre os paradigmas de Orientação a Objetos e conceitos avançados em C#.

- O que são Classes e Objetos?
- O que é uma instância?
- O que são Propriedades?
- O que são Métodos construtores?
- O que é o Garbage Collector?
- O que é Object Dispose?
- Defina os modificadores public, private e protected
- O que são objetos estáticos?
- O que é Herança?
- O que é Upcast e Downcast?
- O que são Interfaces?
- O que são Classes abstratas?
- Qual a finalidade das Classes seladas?
- O que é Sobrecarga de métodos?
- O que é Sobrescrita de método?
- Como podemos Comparar dois objetos no C#?
- Qual a finalidade do Dispose?
- O que é Encapsulamento?
- O que é Polimorfismo?
- O que são Tipos complexos?
- O que são Delegates?
- O que são events?
- Qual a diferença entre Events e Delegates?
- O que são os generics?
- Como restringimos um tipo genérico?

### [Tratamento de Erros e Exceções](categorias/09_tratamento_de_erros_e_excecoes.md)
Melhores práticas para o manejo de erros e exceções em aplicações .NET.

- Como tratamos erros no C#?
- Qual a finalidade do finally?
- Para que serve o Try/Parse?

### [Concorrência e Assincronismo](categorias/10_concorrencia_e_assincronismo.md)
Discussões sobre técnicas de programação concorrente e assíncrona em C#.

- O que são Tasks?
- Para que serve async/await?
- Qual a diferença entre Task.FromResult e o uso de await?

### [Interfaces e Extensibilidade](categorias/11_interfaces_e_extensibilidade.md)
Como interfaces são usadas para criar sistemas extensíveis e flexíveis em C#.

- Para que usamos a interface IEquatable?
- Para que usamos a interface IComparable?
- Quando utilizamos a interface IDisposable?
- O que são Extension methods?

### [Comandos de Linha de Comando e Ferramentas de Desenvolvimento](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md)
Informações sobre ferramentas de desenvolvimento e comandos de linha de comando úteis no ecossistema .NET.

- Qual comando para executar uma aplicação .NET?
- Qual comando para compilar uma aplicação .NET?
- Qual comando para publicar uma aplicação .NET?
- O que significa Debug?
- Como executamos uma aplicação .NET em modo Debug?

## 🦸 Autor

<sub><b>Lucas Apoena</b></sub></a> <a href="https://www.lucasapoena.eti.br/" title="Smile">🙂</a>
<br />

<p align="left">
    <a href="https://www.linkedin.com/in/lucasapoena/"><img src="https://img.shields.io/badge/-lucasapoena-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
    <a href="https://medium.com/@lucasapoena"><img src="https://img.shields.io/badge/-@lucasapoena-%2312100E?style=flat&logo=medium&logoColor=white"/></a>
    <a href="mailto:contato@lucasapoena.eti.br"><img src="https://img.shields.io/badge/-contato@lucasapoena.eti.br-D14836?style=flat&logo=Gmail&logoColor=white"/></a>
</p>

## Contribuições ✨

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://www.lucasapoena.eti.br/"><img src="https://avatars.githubusercontent.com/u/135553?v=4?s=100" width="100px;" alt="Lucas Apoena"/><br /><sub><b>Lucas Apoena</b></sub></a><br /><a href="https://github.com/lucasapoena/dotnet-faq/commits?author=lucasapoena" title="Documentation">📖</a> <a href="https://github.com/lucasapoena/dotnet-faq/commits?author=lucasapoena" title="Code">💻</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

Contribuições para o repositório são bem-vindas. Se você gostaria de adicionar mais perguntas, respostas, ou melhorar as existentes, por favor, sinta-se à vontade para abrir um pull request.

### 💪 Como contribuir para o projeto

1. Faça um **fork** do projeto.
2. Crie uma nova branch com as suas alterações: `git checkout -b my-feature`
3. Salve as alterações e crie uma mensagem de commit contando o que você fez: `git commit -m "feature: My new feature"`
4. Envie as suas alterações: `git push origin my-feature`

## 📝 Licença

Este projeto é distribuído sob a licença [MIT](LICENSE).

## Agradecimentos

Um agradecimento especial ao [Balta](https://balta.io) por criar e compartilhar o artigo original que inspirou a criação deste repositório.