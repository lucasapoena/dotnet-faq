# Repositório de Perguntas e Respostas sobre .NET
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Este repositório contém uma coleção de perguntas e respostas voltadas para a linguagem C# e a plataforma .NET. É um recurso útil para aqueles que estão se preparando para entrevistas de emprego, estudando para certificações ou simplesmente buscando aprimorar seus conhecimentos no .NET Framework, .NET Core e .NET 5/6.

As perguntas foram originadas de um artigo criado por [André Baltieri](https://balta.io), também conhecido como Balta, e podem ser acessadas no seguinte link: [Perguntas para entrevistas de C#](https://balta.io/blog/perguntas-entrevista-csharp).

<table>
  <tr>
    <th>Nível</th>
    <th>Conhecimentos Esperados</th>
  </tr>
  <tr>
    <td>Estagiário</td>
    <td>
      <ul>
        <li>Linguagem de Programação</li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Júnior</td>
    <td>
      <ul>
        <li>Tópicos do Nível Estagiário</li>
        <li>Saber um pouco sobre Orientação a Objeto (POO)</li>
        <li>Saber pesquisar os problemas e se virar bem consultando Google/Amigos/etc</li>
        <li>Conseguir fazer uma API com alguma ajuda caso necessário</li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Pleno</td>
    <td>
      <ul>
        <li>Tópicos do Nível Júnior e demais</li>
        <li>Saber muito bem sobre Orientação a Objeto (POO)</li>
        <li>Conhecer um pouco sobre Arquitetura (MVC, estruturas de projeto)</li>
        <li>Realizar entregas com tranquilidade</li>
        <li>Conseguir criar APIs sem muito esforço</li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Senior</td>
    <td>
      <ul>
        <li>Tópicos do Nível Pleno e demais</li>
        <li>Possuir vivência no desenvolvimento de soluções</li>
        <li>Conhecer bem sobre Arquitetura de Software</li>
        <li>Se responsabilizar pelo direcionamento técnico do projeto</li>        
        <li>Conseguir auxiliar os demais integrantes do time na parte técnica</li>        
      </ul>   
    </td>
  </tr>
</table>

Para enriquecer e refinar as respostas a algumas das questões apresentadas, recorremos ao auxílio do ChatGPT-4. Sinta-se encorajado a aprimorar as respostas conforme necessário.

## Categorias

As perguntas estão organizadas por tópicos para facilitar o acesso e o estudo:

### [Fundamentos e Conceitos Básicos](categorias/01_fundamentos_e_conceitos_basicos.md)
Questões sobre os princípios fundamentais do .NET e os conceitos básicos de C#.

<table>
  <tr>
    <th>Nível</th>
    <th>Perguntas</th>
  </tr>
  <tr>
    <td>Estagiário</td>
    <td>
      <ul>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-c-é-uma-linguagem-compilada-tipada-e-gerenciada-o-que-isto-significa">O C# é uma linguagem compilada, tipada e gerenciada, o que isto significa?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-diferencia-uma-linguagem-compilada-de-uma-interpretada">O que diferencia uma linguagem compilada de uma interpretada?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-o-clr">O que é o CLR?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-il">O que é IL?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-um-framework">O que é um Framework?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-o-net">O que é o .NET?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-o-net-standard">O que é o .NET Standard?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-significa-lts-na-versão-do-software">O que significa LTS na versão do software?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-um-runtime">O que é um Runtime?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-um-sdk">O que é um SDK?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-um-cli">O que é um CLI?</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#o-que-é-uma-solution">O que é uma Solution?</a></li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Júnior</td>
    <td>
      <ul>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#explique-como-o-c-funciona">Explique como o C# funciona</a></li>
        <li><a href="categorias/01_fundamentos_e_conceitos_basicos.md/#explique-o-que-é-versão-semântica">Explique o que é versão semântica?</a></li>
      </ul>   
    </td>
  </tr>
</table>


### [Estrutura de Projetos e Soluções](categorias/02_estrutura_de_projetos_e_solucoes.md)
Detalhes sobre como projetos e soluções são estruturados em um ambiente .NET.

<table>
  <tr>
    <th>Nível</th>
    <th>Perguntas</th>
  </tr>
  <tr>
    <td>Estagiário</td>
    <td>
      <ul>
        <li><a href="categorias/02_estrutura_de_projetos_e_solucoes.md/#cite-3-tipos-de-projetos-que-temos-no-net">Cite 3 tipos de projetos que temos no .NET</a></li>
        <li><a href="categorias/02_estrutura_de_projetos_e_solucoes.md/#qual-nome-do-método-principal-de-um-console-app">Qual nome do método principal de um Console App?</a></li>
        <li><a href="categorias/02_estrutura_de_projetos_e_solucoes.md/#o-que-são-namespaces">O que são Namespaces?</a></li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Júnior</td>
    <td>
      <ul>
        <li><a href="categorias/02_estrutura_de_projetos_e_solucoes.md/#qual-a-finalidade-da-pasta-properties">Qual a finalidade da pasta Properties?</a></li>
        <li><a href="categorias/02_estrutura_de_projetos_e_solucoes.md/#qual-a-finalidade-das-pastas-bin-e-obj">Qual a finalidade das pastas Bin e Obj?</a></li>
      </ul>   
    </td>
  </tr>
</table>

### [Programação Básica em C#](categorias/03_programacao_basica_csharp.md)
Perguntas que cobrem a sintaxe básica e as construções da linguagem C#.

<table>
  <tr>
    <th>Nível</th>
    <th>Perguntas</th>
  </tr>
  <tr>
    <td>Estagiário</td>
    <td>
      <ul>
        <li><a href="categorias/03_programacao_basica_csharp.md/#quais-partes-compõe-um-programa-em-c">Quais partes compõe um programa em C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-diferença-entre-uma-variável-e-uma-constante">Qual a diferença entre uma variável e uma constante?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#quais-formas-temos-de-comentar-código-em-c">Quais formas temos de comentar código em C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-tipos-primitivos">O que são tipos primitivos?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-valor-padrão-do-tipo-char">Qual valor padrão do tipo char?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-tipos-nulos">O que são tipos nulos?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-conversões-implícitas">O que são conversões implícitas?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-conversões-explícitas">O que são conversões explícitas?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-operadores-aritméticos-e-quais-temos-no-c">O que são operadores aritméticos e quais temos no C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-operadores-de-atribuição-e-quais-temos-no-c">O que são operadores de atribuição e quais temos no C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-operadores-de-comparação-e-quais-temos-no-c">O que são operadores de comparação e quais temos no C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-operadores-lógicos-e-quais-temos-no-c">O que são operadores lógicos e quais temos no C#?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#cite-duas-estruturas-condicionais-que-temos-no-c">Cite duas estruturas condicionais que temos no C#</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#cite-duas-estruturas-de-repetição-que-temos-no-c">Cite duas estruturas de repetição que temos no C#</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-finalidade-do-using">Qual a finalidade do Using?</a></li>
      </ul>   
    </td>
  </tr>
  <tr>
    <td>Júnior</td>
    <td>
      <ul>
        <li><a href="categorias/03_programacao_basica_csharp.md/#cite-3-nomes-reservados-que-temos-no-c">Cite 3 nomes reservados que temos no C#</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-tipo-base-no-net">Qual tipo base no .NET?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#dado-um-var-de-um-número-inteiro-qual-tipo-seria-o-var">Dado um var de um número inteiro, qual tipo seria o var?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#dado-um-var-de-um-número-real-qual-tipo-seria-o-var">Dado um var de um número real, qual tipo seria o var?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-diferença-entre-char-e-string">Qual a diferença entre char e string?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-diferença-entre-var-e-object">Qual a diferença entre var e object?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-alias-cite-3-exemplos">O que são alias? Cite 3 exemplos</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-diferença-entre-parse-e-convert">Qual a diferença entre parse e Convert?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-diferença-entre-while-e-dowhile">Qual a diferença entre while e do/while?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-heap-e-stack">O que são heap e stack?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-tipos-de-valor-e-tipos-de-referência">O que são tipos de valor e tipos de referência?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#onde-são-armazenados-os-tipos-de-valor">Onde são armazenados os tipos de valor?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#onde-são-armazenados-os-tipos-de-referência">Onde são armazenados os tipos de referência?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-structs">O que são Structs?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-são-enumeradores">O que são enumeradores?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#o-que-é-um-guid">O que é um GUID?</a></li>
        <li><a href="categorias/03_programacao_basica_csharp.md/#qual-a-finalidade-do-mathround-mathceiling-e-mathfloor">Qual a finalidade do Math.Round, Math.Ceiling e Math.Floor?</a></li>
      </ul>   
    </td>
  </tr>
</table>

### [Métodos e Parâmetros](categorias/04_metodos_e_parametros.md)
Explicações sobre a definição e utilização de métodos e a passagem de parâmetros em C#.

- [x] [Como definimos que um método não retorna valor algum?](categorias/04_metodos_e_parametros.md#como-definimos-que-um-método-não-retorna-valor-algum)
- [x] [Podemos ter métodos sem parâmetros no C#?](categorias/04_metodos_e_parametros.md#podemos-ter-métodos-sem-parâmetros-no-c)
- [x] [Como tornamos um parâmetro opcional no C#?](categorias/04_metodos_e_parametros.md#como-tornamos-um-parâmetro-opcional-no-c)


### [Strings e Manipulação de Texto](categorias/05_strings_e_manipulacao_de_texto.md)
Questões focadas na manipulação de strings e operações com texto no C#.

- [x] [O que é interpolação de String?](categorias/05_strings_e_manipulacao_de_texto.md#o-que-é-interpolação-de-string)
- [x] [Qual a finalidade do método CompareTo?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-compareto)
- [x] [Qual a finalidade do método Contains?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-contains)
- [x] [Qual a finalidade do método StartsWith e EndsWith?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-startswith-e-endswith)
- [x] [Qual a finalidade do método Equals?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-equals)
- [x] [Qual a finalidade do método IndexOf e LastIndexOf?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-indexof-e-lastindexof)
- [x] [Qual a finalidade do método ToLower e ToUpper?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-tolower-e-toupper)
- [x] [Qual a finalidade do método Insert?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-insert)
- [x] [Qual a finalidade do método Length?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-length)
- [x] [Qual a finalidade do método Remove?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-remove)
- [x] [Qual a finalidade do método Replace?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-replace)
- [x] [Qual a finalidade do método Split?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-split)
- [x] [Qual a finalidade do método Substring?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-substring)
- [x] [Qual a finalidade do método Trim?](categorias/05_strings_e_manipulacao_de_texto.md#qual-a-finalidade-do-método-trim)
- [x] [O que é StringBuilder e quando devemos utilizar?](categorias/05_strings_e_manipulacao_de_texto.md#o-que-é-stringbuilder-e-quando-devemos-utilizar)
- [x] [O que é Regex e quando devemos utilizar?](categorias/05_strings_e_manipulacao_de_texto.md#o-que-é-regex-e-quando-devemos-utilizar)


### [Data, Hora e Timezones](categorias/06_data_hora_e_timezones.md)
Como lidar com datas, horas e fusos horários em aplicações .NET.

- [x] [O que é o DateTime?](categorias/06_data_hora_e_timezones.md#o-que-é-o-datetime)
- [x] [Como obtemos a data de hoje no C#?](categorias/06_data_hora_e_timezones.md#como-obtemos-a-data-de-hoje-no-c)
- [x] [Como convertemos uma data para String?](categorias/06_data_hora_e_timezones.md#como-convertemos-uma-data-para-string)
- [x] [Como comparamos duas datas em C#?](categorias/06_data_hora_e_timezones.md#como-comparamos-duas-datas-em-c)
- [x] [Como podemos obter o ano, mês ou dia no C#?](categorias/06_data_hora_e_timezones.md#como-podemos-obter-o-ano-mês-ou-dia-no-c)
- [x] [Como podemos obter o último dia do mês no C#?](categorias/06_data_hora_e_timezones.md#como-podemos-obter-o-último-dia-do-mês-no-c)
- [x] [Podemos criar datas nulas?](categorias/06_data_hora_e_timezones.md#podemos-criar-datas-nulas)
- [x] [O que é Timezone?](categorias/06_data_hora_e_timezones.md#o-que-é-timezone)
- [x] [Como obtermos a data sem um Timezone no C#?](categorias/06_data_hora_e_timezones.md#como-obtermos-a-data-sem-um-timezone-no-c)
- [x] [O que é DateTime Offset?](categorias/06_data_hora_e_timezones.md#o-que-é-datetime-offset)
- [x] [O que é um TimeSpan?](categorias/06_data_hora_e_timezones.md#o-que-é-um-timespan)

### [Coleções, Listas e Generics](categorias/07_colecoes_listas_e_generics.md)
Exploração do uso de coleções, listas e tipos genéricos no C#.

- [ ] [Qual a diferença entre IEnumerable, IList e ICollection?](categorias/07_colecoes_listas_e_generics.md#qual-a-diferença-entre-ienumerable-ilist-e-icollection)
- [ ] [Qual a diferença entre List e IList?](categorias/07_colecoes_listas_e_generics.md#qual-a-diferença-entre-list-e-ilist)
- [ ] [Qual a finalidade do método Add e AddRange em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-add-e-addrange-em-uma-lista)
- [ ] [Qual a finalidade do método Clear em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-clear-em-uma-lista)
- [ ] [Qual a finalidade do método Contains em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-contains-em-uma-lista)
- [ ] [Qual a finalidade do método CopyTo em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-copyto-em-uma-lista)
- [ ] [Qual a finalidade do método Exists em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-exists-em-uma-lista)
- [ ] [Qual a finalidade do método Find e FindAll em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-find-e-findall-em-uma-lista)
- [ ] [Qual a finalidade do método IndexOf e LastIndexOf em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-indexof-e-lastindexof-em-uma-lista)
- [ ] [Qual a finalidade do método FindIndex, FindLast e FindLastIndex em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-findindex-findlast-e-findlastindex-em-uma-lista)
- [ ] [Qual a finalidade do método Insert e InsertRange em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-insert-e-insertrange-em-uma-lista)
- [ ] [Qual a finalidade do método Remove, RemoveAll, RemoveAt e RemoveRange em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-remove-removeall-removeat-e-removerange-em-uma-lista)
- [ ] [Qual a finalidade do método Reverse em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-reverse-em-uma-lista)
- [ ] [Qual a finalidade do método Sort em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-sort-em-uma-lista)
- [ ] [Qual a finalidade do método ToArray em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-toarray-em-uma-lista)
- [ ] [Qual a finalidade do método TrueForAll em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-trueforall-em-uma-lista)
- [ ] [Qual a finalidade do método ConvertAll em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-convertall-em-uma-lista)
- [ ] [Qual a finalidade do método ForEach em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-foreach-em-uma-lista)
- [ ] [Qual a finalidade do método Where em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-where-em-uma-lista)
- [ ] [Qual a finalidade do método First em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-first-em-uma-lista)
- [ ] [Qual a finalidade do método OrderBy em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-orderby-em-uma-lista)
- [ ] [Qual a finalidade do método Select em uma lista?](categorias/07_colecoes_listas_e_generics.md#qual-a-finalidade-do-método-select-em-uma-lista)


### [Orientação a Objetos e Conceitos Avançados](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md)
Questões aprofundadas sobre os paradigmas de Orientação a Objetos e conceitos avançados em C#.

- [ ] [O que são Classes e Objetos?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-classes-e-objetos) (Júnior)
- [ ] [O que é uma instância?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-uma-instância)
- [ ] [O que são Propriedades?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-propriedades)
- [ ] [O que são Métodos construtores?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-métodos-construtores)
- [ ] [O que é o Garbage Collector?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-o-garbage-collector)
- [ ] [O que é Object Dispose?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-object-dispose)
- [ ] [Defina os modificadores public, private e protected](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#defina-os-modificadores-public-private-e-protected) (Júnior)
- [ ] [O que são objetos estáticos?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-objetos-estáticos)
- [ ] [O que é Herança?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-herança) (Júnior)
- [ ] [O que é Upcast e Downcast?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-upcast-e-downcast)
- [ ] [O que são Interfaces?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-interfaces) (Júnior)
- [ ] [O que são classes abstratas?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-classes-abstratas) (Júnior)
- [ ] [Qual a finalidade das classes seladas (sealed class)?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#qual-a-finalidade-das-classes-seladas) (Júnior)
- [ ] [O que é Sobrecarga de métodos?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-sobrecarga-de-métodos) (Júnior)
- [ ] [O que é Sobrescrita de método?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-sobrescrita-de-método) (Júnior)
- [ ] [Como podemos Comparar dois objetos no C#?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#como-podemos-comparar-dois-objetos-no-c)
- [ ] [Qual a finalidade do Dispose?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#qual-a-finalidade-do-dispose)
- [ ] [O que é Encapsulamento?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-encapsulamento) (Júnior)
- [ ] [O que é Polimorfismo?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-é-polimorfismo) (Júnior)
- [ ] [O que são Tipos complexos?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-tipos-complexos)
- [ ] [O que são Delegates?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-delegates)
- [ ] [O que são events?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-events)
- [ ] [Qual a diferença entre Events e Delegates?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#qual-a-diferença-entre-events-e-delegates)
- [ ] [O que são os generics?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#o-que-são-os-generics)
- [ ] [Como restringimos um tipo genérico?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md#como-restringimos-um-tipo-genérico)
- [ ] [O que são partial class?](categorias/08_orientacao_a_objetos_e_conceitos_avancados.md)


### [Tratamento de Erros e Exceções](categorias/09_tratamento_de_erros_e_excecoes.md)
Melhores práticas para o manejo de erros e exceções em aplicações .NET.

- [ ] [Como tratamos erros no C#?](categorias/09_tratamento_de_erros_e_excecoes.md#como-tratamos-erros-no-c)
- [ ] [Qual a finalidade do finally?](categorias/09_tratamento_de_erros_e_excecoes.md#qual-a-finalidade-do-finally)
- [ ] [Para que serve o Try/Parse?](categorias/09_tratamento_de_erros_e_excecoes.md#para-que-serve-o-tryparse)

### [Concorrência e Assincronismo](categorias/10_concorrencia_e_assincronismo.md)
Discussões sobre técnicas de programação concorrente e assíncrona em C#.

- [ ] [O que são Tasks?](categorias/10_concorrencia_e_assincronismo.md#o-que-são-tasks)
- [ ] [Para que serve async/await?](categorias/10_concorrencia_e_assincronismo.md#para-que-serve-asyncawait)
- [ ] [Qual a diferença entre Task.FromResult e o uso de await?](categorias/10_concorrencia_e_assincronismo.md#qual-a-diferença-entre-taskfromresult-e-o-uso-de-await)

### [Interfaces e Extensibilidade](categorias/11_interfaces_e_extensibilidade.md)
Como interfaces são usadas para criar sistemas extensíveis e flexíveis em C#.

- [ ] [Para que usamos a interface IEquatable?](categorias/11_interfaces_e_extensibilidade.md#para-que-usamos-a-interface-iequatable)
- [ ] [Para que usamos a interface IComparable?](categorias/11_interfaces_e_extensibilidade.md#para-que-usamos-a-interface-icomparable)
- [ ] [Quando utilizamos a interface IDisposable?](categorias/11_interfaces_e_extensibilidade.md#quando-utilizamos-a-interface-idisposable)
- [ ] [O que são Extension methods?](categorias/11_interfaces_e_extensibilidade.md#o-que-são-extension-methods)

### [Comandos de Linha de Comando e Ferramentas de Desenvolvimento](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md)
Informações sobre ferramentas de desenvolvimento e comandos de linha de comando úteis no ecossistema .NET.

- [ ] [Qual comando para executar uma aplicação .NET?](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md#qual-comando-para-executar-uma-aplicação-net)
- [ ] [Qual comando para compilar uma aplicação .NET?](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md#qual-comando-para-compilar-uma-aplicação-net)
- [ ] [Qual comando para publicar uma aplicação .NET?](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md#qual-comando-para-publicar-uma-aplicação-net)
- [ ] [O que significa Debug?](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md#o-que-significa-debug)
- [ ] [Como executamos uma aplicação .NET em modo Debug?](categorias/12_comandos_de_linha_de_comando_e_ferramentas_de_desenvolvimento.md#como-executamos-uma-aplicação-net-em-modo-debug)


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