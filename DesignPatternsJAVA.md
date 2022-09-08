pag 3

> **A programação estruturada:**
- Nesse novo paradigma surgiram estruturas de controle que permitiam a criação de comando condicionais, como o if e o switch, e comandos iterativos, como o for e o while. Uma outra adição importante foram as funções. A partir delas era possível dividir a lógica do programa, permitindo sua modularização. Isso facilita que essas funções possam ser reutilizadas em outras aplicações. 
  - Problemas:
    - A maior dificuldade nesse paradigma era como lidar com os dados e o comportamento associado a eles. 
    - Criação de variáveis globais, que facilmente poderiam acabar causando problemas por estarem com valores inconsistentes. 
    - Dados relacionados que podiam ser livremente modificados e facilmente ficarem inconsistentes.

> **Programação orientada a objetos**
- Além da estruturação da lógica, com esse paradigma era possível a **estruturação dos dados e conceitos do software**. Sendo assim, pode-se colocar toda lógica relacionada a um conjunto de dados junto com ele. Além disso, a partir da possibilidade de abstração de conceitos consegue-se desacoplar componentes, obtendo um maior reúso e uma maior flexibilidade.

- Classes e Objetos:
  - Classe: representa uma abstração dos seus conceitos.  possui estado e comportamento, que são representados respectivamente pelos atributos e métodos definidos.
  - Objeto: um objeto representa uma entidade concreta.  possui um valor para aquela característica. 
  - **É importante perceber que os objetos representam entidades concretas do seu sistema, enquanto as classes abstraem suas características.**

- A **herança** é uma característica do paradigma orientado a objetos que permite que abstrações possam ser definidas em diversos níveis. 

- O **encapsulamento** é um conceito importante da orientação a objetos que diz que deve haver uma separação entre o comportamento interno de uma classe com a interface que ela disponibiliza para os seus clientes.


## Quando devo utilizar uma classe abstrata e quando devo utilizar uma interface?
- Quando a abstração que precisar ser criada for um conceito, ou seja, algo que possa ser refinado e  espacializado, deve-se utilizar uma classe abstrata. Quando a abstração é um comportamento, ou seja, algo que uma classe deve saber fazer, então a melhor solução é a criação de uma interface.

<br/>
<br/>
<br/>

- O **polimorfismo** é na verdade uma consequência da utilização de herança e da utilização de interfaces.
  - A palavra polimorfismo significa "múltiplas formas”, o que indica que um objeto pode assumir a forma de uma de suas abstrações

# Reuso Através de Herança
- `“Entidades de software devem ser abertas a extensão, mas fechadas a modificação.” – Bertrand Meyer`

> O potencial de reúso possível com herança está em outro local! Ele pode estar sim no reúso de código da superclasse, porém não é com a subclasse chamando métodos da superclasse, mas com a superclasse chamando código da subclasse.
>   - isso permite que um mesmo algoritmo possa ser reutilizado com passos alterados


## HOOK METHOD

<img src="https://raw.githubusercontent.com/jcarloscody/teoria_designPatterns/main/img/hoock%20method.PNG">

```
A superclasse possui um método principal público que é invocado pelos seus clientes. Esse método delega parte de sua execução para o hook method, que é um método abstrato que deve ser implementado pela subclasse. Ele funciona como um “gancho” no qual uma nova lógica de execução para a classe pode ser “pendurada”. Cada subclasse o implementa provendo uma lógica diferente. Como essa lógica pode ser invocada a partir do mesmo método público, definido na superclasse, os hook methods permitem que o objeto possua um comportamento diferente de acordo com a subclasse instanciada.
```