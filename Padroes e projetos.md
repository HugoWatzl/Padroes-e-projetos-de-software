## Resumo Simples para Estudo: Padrões de Projeto (Cap. 6)

### O que são Padrões de Projeto?
Pense neles como uma **"receita de bolo"** para resolver problemas comuns no desenvolvimento de software. Não são códigos prontos, mas sim **soluções testadas e comprovadas** que descrevem como estruturar suas classes e objetos.

O principal benefício é criar um **vocabulário comum** entre desenvolvedores, facilitando a **comunicação** e o entendimento de projetos complexos.

### As 3 Categorias (GoF)
1.  **Criacionais:** Lidam com a **criação de objetos** de forma flexível.
    * **Fábrica (Factory):** Centraliza a lógica de criação de objetos, escondendo do cliente qual classe concreta está sendo instanciada.
    * **Singleton:** Garante que uma classe tenha **apenas uma instância** em todo o sistema e fornece um ponto de acesso global a ela.

2.  **Estruturais:** Lidam com a **composição de classes e objetos** para formar estruturas maiores.
    * **Adapter:** "Traduz" a interface de uma classe para outra que o cliente espera, permitindo que classes incompatíveis trabalhem juntas.
    * **Facade:** Oferece uma interface simplificada para um sistema complexo, escondendo suas partes internas.

3.  **Comportamentais:** Lidam com a **interação e a divisão de responsabilidades** entre objetos.
    * **Strategy:** Permite que um algoritmo seja selecionado e trocado em tempo de execução. Encapsula diferentes "estratégias" em classes separadas.
    * **Observer:** Define um mecanismo de assinatura onde múltiplos objetos (Observadores) são notificados automaticamente quando o estado de um objeto (Sujeito) muda.

### Padrão Arquitetural: MVC (Model-View-Controller)
O MVC não é um Padrão de Projeto do GoF, mas sim um **Padrão Arquitetural**. Sua função é **separar as responsabilidades** da aplicação em três camadas, o que facilita muito a manutenção:
* **Model (Modelo):** Representa os dados e a lógica de negócio.
* **View (Visão):** É a interface do usuário, aquilo que ele vê e com o que interage.
* **Controller (Controlador):** Atua como um intermediário, recebendo entradas do usuário (da View) e acionando as devidas atualizações no Model.

---

## Perguntas para Estudo (Baseadas no Resumo)

#### Múltipla Escolha

1.  **Quais são as categorias dos padrões de projeto do GoF?**<br>
    a) Geracionais, Estruturais, Visuais<br>
    b) Criacionais, Estruturais, Comportamentais<br>
    c) Funcionais, Estruturais, Comportamentais<br>
    d) Criacionais, Lógicos, Comportamentais<br>
    e) Comportamentais, de Dados, Estruturais

    <details>
      <summary>Clique para ver a resposta</summary>
      **b) Criacionais, Estruturais, Comportamentais**<br>
      *Justificativa: Conforme o resumo, estas são as três categorias de padrões propostas pelo GoF.*
    </details>
    <br>

2.  **Qual das alternativas é um benefício real dos padrões de projeto?**<br>
    a) Eliminam a necessidade de testes<br>
    b) Tornam o código mais lento<br>
    c) Facilitam a comunicação entre desenvolvedores<br>
    d) Impedem qualquer mudança futura no sistema<br>
    e) Substituem a necessidade de um arquiteto de software<br>

    <details>
      <summary>Clique para ver a resposta</summary>
      **c) Facilitam a comunicação entre desenvolvedores**<br>
      *Justificativa: O resumo destaca que um dos principais benefícios é a criação de um "vocabulário comum" para as equipes.*
    </details><br>

3.  **Sobre o padrão Model-View-Controller (MVC), assinale a alternativa correta:**<br>
    a) Une a lógica de dados e a interface em uma única camada.<br>
    b) É um padrão de projeto da categoria Criacional.<br>
    c) Separa a aplicação em camadas (Modelo, Visão, Controlador), facilitando a manutenção.<br>
    d) É usado exclusivamente para criar bancos de dados.<br>
    e) Força o uso da mesma tecnologia para o back-end e o front-end.<br>

    <details>
      <summary>Clique para ver a resposta</summary>
      **c) Separa a aplicação em camadas (Modelo, Visão, Controlador), facilitando a manutenção.**<br>
      *Justificativa: O resumo explica que a função do MVC é exatamente separar as responsabilidades para facilitar a manutenção.*
    </details><br>

#### Verdadeiro ou Falso

4.  **(  ) O padrão de projeto Singleton permite a criação de múltiplas instâncias de uma mesma classe para melhorar o desempenho.**

5.  **(  ) Padrões de projeto servem como um vocabulário comum, ajudando equipes a discutir soluções de forma mais eficiente.**

<details>
      <summary>Clique para ver o gabarito</summary>
      Gabarito: **4 (F), 5 (V)**<br>
      *Justificativa 4: Falso, o Singleton garante apenas UMA instância.*<br>
      *Justificativa 5: Verdadeiro, este é um de seus principais benefícios.*
</details><br>

#### Relacione os Padrões

Relacione os padrões da primeira coluna com seus objetivos na segunda.
(1) Fábrica (Factory)
(2) Singleton
(3) Strategy
(4) Observer

(  ) Permite que um algoritmo seja trocado em tempo de execução.
(  ) Garante que uma classe tenha apenas uma única instância.
(  ) Notifica múltiplos objetos sobre uma mudança de estado.
(  ) Centraliza a criação de objetos, escondendo a lógica do cliente.

<details>
      <summary>Clique para ver a resposta</summary>
      **(3)** Permite que um algoritmo seja trocado em tempo de execução.<br>
      **(2)** Garante que uma classe tenha apenas uma única instância.<br>
      **(4)** Notifica múltiplos objetos sobre uma mudança de estado.<br>
      **(1)** Centraliza a criação de objetos, escondendo a lógica do cliente.
</details><br>

#### Discursivas Curtas

6.  **Qual é a principal aplicação do padrão Singleton?**

<details>
      <summary>Clique para ver a resposta</summary>
      Garantir que exista apenas uma instância de uma classe em todo o sistema, como em um gerenciador de configurações ou de conexão com o banco de dados.
</details><br>

7.  **Descreva um cenário em que o padrão Strategy seria mais adequado do que simplesmente usar `if/else` dentro de um método.**
<details>
      <summary>Clique para ver a resposta</summary>
      Quando existem várias formas de realizar uma tarefa e a escolha pode mudar dinamicamente. Ex: um sistema de e-commerce que calcula o frete de formas diferentes (Sedex, PAC, transportadora) e permite ao usuário escolher qual usar.
</details><br>

8.  **Explique por que a separação de responsabilidades (como no padrão MVC) facilita a manutenção de sistemas grandes.**
<details>
      <summary>Clique para ver a resposta</summary>
      Porque permite que cada camada (dados, interface, controle) seja alterada de forma independente. Uma mudança na cor de um botão (View) não afeta como os dados são salvos (Model), facilitando o trabalho de equipes diferentes e reduzindo o risco de introduzir bugs.
</details><br>