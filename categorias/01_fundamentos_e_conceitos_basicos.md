# Fundamentos e Conceitos Básicos

Este documento abrange perguntas e respostas sobre os fundamentos e conceitos básicos do .NET e da linguagem de programação C#.

## Perguntas e Respostas

### O C# é uma linguagem compilada, tipada e gerenciada, o que isto significa? (Estagiário)
> Nível: Estagiário
> Justificativa: Compreender os conceitos básicos de uma linguagem de programação faz parte do conhecimento inicial para quem está começando na área.

- **Compilada**: O código escrito em C# não é executado diretamente pela máquina. Em vez disso, ele é traduzido para uma forma intermediária pelo compilador e, em seguida, executado por um ambiente de execução, o CLR (Common Language Runtime). Esta abordagem permite que o código seja otimizado para execução mais rápida após a compilação.

- **Tipada**: C# é uma linguagem fortemente tipada. Cada variável e constante tem um tipo definido, como `int`, `float`, `string`, etc., e o compilador verifica a compatibilidade dos tipos durante a compilação. Isso ajuda a prevenir erros em tempo de execução e torna o código mais seguro e previsível.

- **Gerenciada**: O código C# é executado sob a supervisão do CLR, que é responsável por serviços como a coleta de lixo, o que significa liberação automática de memória não utilizada, tratamento de exceções, e segurança do código. Isso abstrai muitos aspectos de baixo nível de gerenciamento de recursos, permitindo que os desenvolvedores se concentrem na lógica do aplicativo.

---

### O que diferencia uma linguagem compilada de uma interpretada? (Estagiário)

**Linguagem Compilada:**
Quando um programa é escrito em uma linguagem compilada, ele passa por um processo de compilação que transforma o código fonte em código de máquina, que é específico para um determinado sistema ou arquitetura. Esse código de máquina é executado diretamente pelo hardware do computador. Exemplos de linguagens compiladas incluem C, C++ e Fortran.

**Linguagem Interpretada:**
Neste caso, o código fonte é executado linha por linha por um interpretador. Não há fase de compilação separada. Em vez disso, o interpretador lê o código fonte e realiza as operações descritas em tempo real. Exemplos de linguagens interpretadas incluem Python, Ruby e JavaScript.

---
### Explique como o C# funciona

Quando você desenvolve um programa em C#, o processo é composto por várias etapas que transformam o código-fonte que você escreve em um programa executável:

1. **Compilação para IL:**
   - O código-fonte em C# é primeiro compilado pelo compilador de C# (`csc.exe`) em um código intermediário chamado IL (Intermediate Language).
   - Esse IL é independente de plataforma, o que significa que ele não é específico para uma máquina ou sistema operacional.

2. **Empacotamento em Assemblies:**
   - Uma vez compilado, o IL é encapsulado em assemblies. Os assemblies são unidades de implantação que contêm os metadados necessários e o próprio código IL.

3. **Execução pelo CLR:**
   - Ao executar o programa, o CLR (Common Language Runtime) carrega esses assemblies.
   - O CLR utiliza um compilador JIT (Just-In-Time) para converter o IL em código de máquina, que é específico para o sistema no qual o programa está sendo executado.
   - Esse código de máquina é então executado diretamente pelo hardware do computador.

Este processo garante que os programas escritos em C# possam ser executados em diferentes plataformas que suportam o .NET, aproveitando as otimizações e garantias de segurança providas pelo ambiente de execução.

---
### O que é o CLR?

O CLR (Common Language Runtime) é a máquina virtual onde os programas .NET são executados. Ele fornece serviços como:

- Carregamento de assemblies
- Compilação Just-In-Time (JIT)
- Gerenciamento de memória (incluindo coleta de lixo)
- Tratamento de exceções
- Segurança

---

### O que é IL?
IL (Intermediate Language) é uma linguagem de baixo nível usada como intermediária entre o código fonte escrito em linguagens .NET (como C#) e o código de máquina que o hardware executa. Quando um programa .NET é compilado, ele é transformado em IL, que é agnóstico em relação à plataforma. O IL é então convertido em código de máquina específico para a plataforma pelo JIT compiler no momento da execução.

---

### O que é um Framework?
Um framework é um conjunto coeso de bibliotecas e/ou ferramentas que fornece uma base sobre a qual os desenvolvedores podem construir aplicativos mais facilmente, sem ter que "reinventar a roda". O framework pode fornecer funcionalidades prontas para uso, padrões e práticas recomendadas, facilitando a criação de soluções robustas e eficientes. O .NET Framework, por exemplo, é uma coleção de bibliotecas e ferramentas que ajudam os desenvolvedores a criar aplicativos para Windows, Web e outras plataformas.

---

### O que é o .NET?
.NET é uma plataforma de desenvolvimento de software criada pela Microsoft que suporta muitas linguagens de programação, como C#, VB.NET e F#. A plataforma .NET é composta por uma grande biblioteca de classes padrão, um ambiente de tempo de execução e um conjunto de ferramentas de desenvolvimento. A ideia por trás do .NET é fornecer uma maneira unificada de construir e executar aplicações, independentemente do dispositivo ou sistema operacional alvo. Ao longo dos anos, o .NET evoluiu e ramificou-se em diferentes plataformas, incluindo .NET Framework, .NET Core e, mais recentemente, .NET 8 e versões subsequentes, que têm como objetivo unificar novamente estas ramificações.

---

### O que é o .NET Standard?
.NET Standard é uma especificação de conjunto de APIs que todas as implementações da plataforma .NET devem suportar. Em outras palavras, é uma base comum para todas as variantes do .NET (como .NET Framework, .NET Core, Xamarin, etc.). O objetivo do .NET Standard é permitir que os desenvolvedores criem bibliotecas que possam ser usadas em qualquer implementação do .NET, sem precisar reescrever ou ajustar o código para cada plataforma. Isso ajuda a garantir a portabilidade do código e a reutilização em diferentes plataformas .NET.

---

### Explique o que é versão semântica

A versão semântica, ou SemVer, é um sistema de versionamento que usa três números: `MAJOR.MINOR.PATCH` (ex: `1.4.2`). Cada número tem um significado específico:

- **MAJOR**: Incrementado quando são feitas mudanças incompatíveis que exigem que o usuário mude algo sobre sua configuração.
- **MINOR**: Incrementado quando são adicionadas novas funcionalidades de maneira compatível com versões anteriores.
- **PATCH**: Incrementado quando são feitas correções de bugs compatíveis com versões anteriores.

A ideia é que, ao seguir o SemVer, os desenvolvedores possam rapidamente entender as mudanças em um software apenas olhando para a versão e decidir se é seguro atualizar ou se precisam fazer mudanças em seu código.

---

### O que significa LTS na versão do software?

**LTS** significa "Long Term Support" (Suporte a Longo Prazo). Quando um software é rotulado como LTS, significa que essa versão específica receberá suporte (como correções de bugs e atualizações de segurança) por um período prolongado, geralmente vários anos. A ideia por trás das versões LTS é fornecer estabilidade para os usuários que não querem ou não podem atualizar o software frequentemente. Eles podem confiar que essa versão será suportada por um longo tempo, sem precisar se preocupar com mudanças disruptivas ou novas características que podem introduzir incompatibilidades.

---

### O que é um Runtime?

Runtime (ou "tempo de execução") refere-se ao ambiente em que um software é executado. Ele fornece todos os recursos necessários para a execução de um programa. Por exemplo, quando você executa um programa escrito em C# no .NET, o .NET Runtime é responsável por gerenciar a memória, executar o código intermediário (bytecode), lidar com exceções e muito mais.

Outros exemplos de runtimes incluem a Java Virtual Machine (JVM) para Java e o Node.js para JavaScript no lado do servidor. O runtime geralmente fornece uma camada de abstração entre o software e o sistema operacional, permitindo que o software seja executado em diferentes sistemas sem modificações.

---
### O que é um SDK?

SDK (Software Development Kit) é um conjunto de ferramentas, bibliotecas, documentação e, muitas vezes, código de exemplo, que permite aos desenvolvedores criar software para uma plataforma ou sistema específico. Um SDK pode incluir compiladores, depuradores e outras utilidades que ajudam os desenvolvedores a construir e otimizar seu software. Ao fornecer estas ferramentas, um SDK pode acelerar o processo de desenvolvimento, pois o desenvolvedor não precisa reinventar funcionalidades básicas e pode focar na lógica específica de sua aplicação.

---
### O que é um CLI?
CLI (Command Line Interface) refere-se a uma interface baseada em texto que permite aos usuários interagir com programas e sistemas operacionais ao inserir comandos específicos por meio do teclado. Diferente das GUIs (Graphical User Interfaces), onde a interação é baseada principalmente em cliques do mouse e widgets visuais, a CLI é inteiramente baseada em texto. CLIs são frequentemente usadas por desenvolvedores e administradores de sistema devido à sua eficiência e capacidade de automação.

---
### O que é uma Solution?

No contexto do ambiente de desenvolvimento da Microsoft, como o Visual Studio, uma **Solution (Solução)** é uma estrutura para organizar um ou mais projetos relacionados. Ela permite que os desenvolvedores agrupem projetos que compartilham recursos comuns, dependências ou que estão relacionados de alguma forma.

Por exemplo, uma Solution pode conter um projeto de aplicativo web, um projeto de biblioteca de classes (que contém a lógica de negócios) e um projeto de teste unitário. Todas essas partes são inter-relacionadas e, ao agrupá-las em uma Solution, torna-se mais fácil gerenciar, construir e implementar o sistema como um todo.

---