# **Padrões de Projeto**
3pag
- **`POO:`** paradigma que tem um conceito que envolve pedaços de dados e que portam comportamentos e estes forma uma coleção de objetos e são construídos sob um plano, as classes.
- **`Classe:`** define a estrutura dos objetos.
- **`Hierarquia de Classes:`**
  - **subclasses** podem sobrescrever o comportamento que herdam das **superclasses**.

## **Pilares POO**
- **`Abstração:`** moldar objetos do programa com base nos objetos do mundo real. e a abstração disto se moldará apenas aos objetivos específicos.
- **`Encapsulamento:`** é tornar as coisas privadas, esconder estados e comportamentos de outros objetos e criar interfaces para acessa-los.
  - **Interfaces:** permite criar contratos de interação entre objetos.
- **`Herança:`** é a habilidade de construir novas classes em cima de classes já existentes.
  - possibilita **reutilizar** codigos.
- **`Polimorfismo:`** é a habilidade de rastrear a classe real de um objeto e chamar sua implementacao mesmo quando seu tipo real é desconhecido no contexto.


## **Relações entre Objetos**
- **`Dependência:`** Existe uma dependência entre duas classes se
algumas mudanças na definição de uma das classes pode resultar em modificações em outra classe.
  - é o mais básico e o mais fraco tipo de relações entre classes.
  - Você pode tornar a dependência
mais fraca se você fazer seu código ser dependente de interfaces ou classes abstratas ao invés de classes concretas.
  - **O ocorre quando usamos em tipos em assinaturas de metodos, quando instanciamos objetos atraves de chamadas do construtor.**
- **`Associação:`** um relacionamento no qual um objeto usa ou
interage com outro.
  - um tipo especializado de dependência.
  - Em geral, você usa uma associação para representar algo como
um campo em uma classe
- **`Agregação:`** é um tipo especializado de associação que representa relações individuais (one-to-many), multiplas(many-to-many), e totais (whole-part) entre multiplos objetos.
  - Geralmente, sob agregação, um objeto “tem” um conjunto de outros objetos e serve como um contêiner ou coleção. O componente pode existir sem o contêiner e pode ser ligado através de vários contêineres ao mesmo tempo.
- **`Composição:`** tipo especifico de agregação.
  - porém aqui o componente só pode existir como parte de um conteiner.


 - **`Dependência:`** Classe A pode ser afetada por mudanças na classe B.
- **`Associação:`** Objeto A sabe sobre objeto B. Classe A depende de B.
- **`Agregação:`** Objeto A sabe sobre objeto B, e consiste de B. Classe A depende de B.
- **`Composição:`** Objeto A sabe sobre objeto B, consiste de B, e gerencia o ciclo de vida de B. Classe A depende de B.
- **`Implementação:`** Classe A define métodos declarados na interface B. objetos de A podem ser tratados como B. Classe A depende de B.
- **`Herança:`** Classe A herda a interface e implementação da classe B mas pode estendê-la. Objets de A podem ser tratados como B. Classe A depende de B.



# **Introdução aos Padrões**
> ## **`O que é um padrão de projeto?`**
- são soluções típicas para problemas comuns em projeto de software.
- Os padrões são soluções típicas para problemas comuns em projetos orientados a objetos. Quando uma solução é repetida de novo e de novo em vários projetos, alguém vai eventualmente colocar um nome para ela e descrever a solução em detalhe. É basicamente assim que um padrão é descoberto.
  
<br/>

- **`Algoritmo VS padrões:`** `algoritmo` é que ele seria uma receita de comida: ambos têm etapas claras para chegar a um objetivo. Por outro lado, um `padrão` é mais como uma planta de obras: você pode ver o resultado e suas funcionalidades, mas a ordem exata de implementação depende de você.
    
<br/>

- **`Do que consiste um padrão?`**
  - **Propósito**: descreve o problema e a solução
  - **Motivação**: explica o problema e a solução
  - **Estruturas**: mostra cada parte do padrão e como se relacionam
  
<br/>

- **`Classificação de Nível`**
  - **Baixo**: são chamados de idiomáticos. geralmente se aplica apenas à uma única linguagem.
  - **Alto**: são o padrões arquitetônicos desenvolvedores podem implementar esses padrões em praticamente qualquer linguagem. Ao contrário de outros padrões, eles podem ser usados para fazer o projeto da arquitetura de toda uma aplicação.

<br/>

- **`Categorias`**:
  - **Padrões criacionais:** mecanismos de criação de
objetos
  - **Padrões estruturais:** montar objetos e classes em estruturas maiores
  - **Padrões comportamentais:** comunicação eficiente e da assinalação de responsabilidades entre objetos.
    
<br/>

- **`Histórico`**
  - A ideia foi seguida por quatro autores: Erich Gamma, John Vlissides, Ralph Johnson, e Richard Helm. Em 1994, eles publicaram Padrões de Projeto - Soluções Reutilizáveis de Software Orientado a Objetos
    - O livro mostrava **23 padrões**
    - livro GoF: o livro da Gangue dos Quatro (Gang of Four)


<br/><br/>

### **`Características de bom Projeto`**
- Reutilização de código
- Extensibilidade

<br/>

> ### **`Princípios`**
 - **Encapsule o que varia**: Identifique os aspectos da sua aplicação que variam e separe-os dos que permanecem os mesmos. a finalidade é minimizar o efeito causado por mudanças.
   - você pode isolar as partes de um programa
que variam em módulos independentes, protegendo o resto do código de efeitos adversos
 - **Encapsulamento à nivel de método** expressa a ideia de separar as responsabilidades de cada método. evitar método de clínico geral.
 - **Encapsulamento a nível de classe**: fazer com que uma classe contenha apenas métodos relacionado a seu objetivo fim.
 - **Programe para uma interface, não uma implementação:** Dependa de abstrações, não classes concretas. Você pode perceber se o projeto é flexível o bastante se você pode estendê-lo facilmente sem quebrar o código existente.
 - **Prefira composição sobre herança:** temos problemas quando temos muitas classes e a mudança fica muito difícil, são eles:
   - *Uma subclasse não pode reduzir a interface da superclasse* vc acaba implementando todos os metodos abstratos da classe mãe mesmo q nao queira.
   - *Quando sobrescrevendo métodos você precisa se certificar que o novo comportamento é compatível com o comportamento base*
   - *A herança quebra o encapsulamento da superclasse*
   - *As subclasses estão firmemente acopladas as superclasses.*
   - *Tentar reutilizar código através da herança pode levar a criação de hierarquias de heranças paralelas.*

Há `uma alternativa para a herança chamada composição`. Enquanto a herança representa uma relação “é um(a)” entre classes (um carro é um transporte), a composição representa a
relação “tem um(a)” (um carro tem um motor).

> ## **`Princípios SOLID`**
```sh
SOLID -  projeto destinados a fazer dos projetos de software 
algo mais compreensivo, flexível, e sustentável.

 Empenhar-se para seguir estes princípios é bom, mas sempre tente 
 ser pragmático e não tome tudo que está escrito aqui como um dogma.
```

- **Single Responsibility Principle - (responsabilidade única)** 
  - Uma classe deve ter apenas uma razão para mudar.
  - fim: reduzir a complexidade.
  - se uma classe faz muitas coisas, você terá que mudá-la cada vez que uma dessas coisas muda.

- **pen/Closed Principle - (aberto/fechado)**
  - As classes devem ser abertas para extensão, mas fechadas para modificação.
  - fim: previnir a quebra quando novas implementações forem realizadas.
  - Aberta: uma classe que pode ser herdada, possui métodos que podem ser sobrescritos.
  - Fechada: classe completa. é fechada para modificação. não pode ser extendida.

- **iskov Substitution Principle (Princípio de substituição de Liskov)**
  - Quando estendendo uma classe, lembre-se que você
deve ser capaz de passar objetos da subclasse em lugar
de objetos da classe mãe sem quebrar o código cliente.
  - foi nomeado por Barbara Liskov, que o definiu em 1987
em seu trabalho Data abstraction and hierarchy


- **Interface Segregation Principle(Princípio de segregação de interface)**
  - Clientes não devem ser forçados a depender de métodos que não usam.
  - Os clientes devem implementar somente aqueles
métodos que realmente precisam. Do contrário, uma mudança
em uma interface “gorda” irá quebrar clientes que nem sequer
usam os métodos modificados.

- **Dependency Inversion Principle (Princípio de inversão de dependência)**
  - Classes de alto nível não deveriam depender de classes de baixo nível. Ambas devem depender de abstrações. As abstrações não devem depender de detalhes. Detalhes devem depender de abstrações.
    - Classes de baixo nível implementam operações básicas tais como trabalhar com um disco, transferindo dados pela rede, conectar-se a uma base de dados, etc.
    - Classes de alto nível contém lógica de negócio complexa que direcionam classes de baixo nível para fazerem algo.


# Padrões de Projeto Criacionais
- Fornecem vários mecanismos de criação de objetos.

## FACTORY METHOD :: Método fábrica, Construtor virtual
- O padrão Factory Method sugere que você substitua chamadas diretas de construção de objetos (usando o operador new ) por chamadas para um método fábrica especial.

<img src="">

- Porém, há uma pequena limitação: as subclasses só podem retornar tipos diferentes de produtos se esses produtos tiverem uma classe ou interface base em comum.

<img src="">

p84