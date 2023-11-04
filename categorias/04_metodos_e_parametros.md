# Métodos e Parâmetros

Este documento explora a definição de métodos em C# e a passagem de parâmetros.

## Perguntas e Respostas

### :grey_question: Como definimos que um método não retorna valor algum?

Em C#, um método que não retorna valor algum é definido usando a palavra-chave `void`. Quando um método é declarado como `void`, ele não pode retornar nenhum valor usando a instrução `return`. Se tentar fazer isso, ocorrerá um erro de compilação. No entanto, o método ainda pode usar a instrução `return` por si só para sair prematuramente do método.

Aqui está um exemplo de um método que não retorna valor:

```csharp
public void ExibirMensagem()
{
    Console.WriteLine("Este método não retorna valor algum.");
    // Não é necessário usar 'return', mas poderia ser usado para sair do método.
}
```

---
### :grey_question: Podemos ter métodos sem parâmetros no C#?

Sim, no C# é perfeitamente possível ter métodos que não requerem parâmetros. Estes são chamados de métodos sem parâmetros, e eles realizam ações sem a necessidade de informações adicionais externas.

Aqui está um exemplo de um método sem parâmetros:

```csharp
public void Saudar()
{
    Console.WriteLine("Olá, mundo!");
}
```

Neste exemplo, o método `Saudar()` pode ser chamado sem passar nenhum argumento.

---
### :grey_question: Como tornamos um parâmetro opcional no C#?

Em C#, você pode tornar um parâmetro opcional ao definir um valor padrão para ele na declaração do método. Quando um argumento correspondente a um parâmetro opcional não é fornecido, o valor padrão é usado. Parâmetros opcionais devem ser definidos após todos os parâmetros obrigatórios na lista de parâmetros do método.

Aqui está um exemplo de como criar um parâmetro opcional:

```csharp
public void ConfigurarAlerta(string mensagem, bool beep = false)
{
    Console.WriteLine(mensagem);
    if (beep)
    {
        Console.Beep();
    }
}
```

No exemplo acima, `beep` é um parâmetro opcional com um valor padrão de `false`. Isso significa que você pode chamar `ConfigurarAlerta("Aviso importante!")` sem especificar um valor para `beep`, e ele usará o valor padrão.

---