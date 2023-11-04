# Fundamentos e Conceitos Básicos

Este documento abrange perguntas e respostas sobre os fundamentos e conceitos básicos do .NET e da linguagem de programação C#.

## Perguntas e Respostas

### O C# é uma linguagem compilada, tipada e gerenciada, o que isto significa?

- **Compilada**: O código escrito em C# não é executado diretamente pela máquina. Em vez disso, ele é traduzido para uma forma intermediária pelo compilador e, em seguida, executado por um ambiente de execução, o CLR (Common Language Runtime). Esta abordagem permite que o código seja otimizado para execução mais rápida após a compilação.

- **Tipada**: C# é uma linguagem fortemente tipada. Cada variável e constante tem um tipo definido, como `int`, `float`, `string`, etc., e o compilador verifica a compatibilidade dos tipos durante a compilação. Isso ajuda a prevenir erros em tempo de execução e torna o código mais seguro e previsível.

- **Gerenciada**: O código C# é executado sob a supervisão do CLR, que é responsável por serviços como a coleta de lixo, o que significa liberação automática de memória não utilizada, tratamento de exceções, e segurança do código. Isso abstrai muitos aspectos de baixo nível de gerenciamento de recursos, permitindo que os desenvolvedores se concentrem na lógica do aplicativo.

---

### O que diferencia uma linguagem compilada de uma interpretada?

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
---
### O que é um Framework?
---
### O que é o .NET?
---
### O que é o .NET Standard?
---
### O que significa LTS na versão do software?
---
### O que é um Runtime?
---
### O que é um SDK?
---
### O que é um CLI?
---
### O que é uma Solution?
---
### Explique o que é versão semântica?
---