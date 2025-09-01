# DESIGN-E-ARQUITETURA-DE-SOFTWARE
Repositório da disciplina de Design e Arquitetura de Software (Univille/2025). Contém resumos, estudos e exercícios sobre princípios, padrões arquiteturais (camadas, MVC, microserviços), atributos de qualidade e boas práticas no desenvolvimento de software.

# Aula 00- 28/07/2025
## Anotações da Aula

- Disciplina voltada para **conceitos de design e arquitetura de software**.  
- Diferença em relação à Fábrica de Software: foco **teórico e conceitual**, não em projetos práticos.  
- Importância no mercado: escalabilidade, desempenho, manutenção e qualidade de sistemas.  
- Papel do arquiteto de software:  
  - Definir arquitetura.  
  - Orientar desenvolvedores.  
  - Evitar **débito técnico**.  

---

## Conceitos Iniciais
- **Débito Técnico** = consequências de decisões ruins → dificulta evolução e manutenção.  
- **Arquitetura em Camadas**: Entidades → Repositórios → Serviços → Controllers.  
- **MVC** (Model-View-Controller): separação entre dados, lógica e interface.  
- **Monólito x Microsserviços**: diferenças de estrutura e aplicação.  

---

## Materiais
- Livro gratuito: *Engenharia de Software Moderna* (Prof. Túlio – UFMG).  
- Livro da Biblioteca Virtual Univille: *Fundamentos de Arquitetura de Software* (2023/24).  

---

## Tarefas
1. Criar repositório no GitHub → `design-arquitetura-software`.  
2. Adicionar professor como colaborador.  
3. Registrar resumos e exercícios a cada aula.  

---

# Aula 01- 31/07/2025

Nesta aula, foram abordados conceitos fundamentais de arquitetura e desenvolvimento de software, focando em boas práticas para gerenciar a complexidade e criar sistemas robustos e flexíveis.


## Tópicos Principais

### Abstração: A Essência do Software
* O principal trabalho no desenvolvimento de software é a **abstração**: entender um problema do mundo real e representá-lo em código.
* Exemplos práticos do projeto anterior (Fábrica de Software) foram citados, como a criação de `Entidades` para representar dados, `Repositórios` para abstrair o acesso ao banco de dados, `Serviços` para a lógica de negócio e `Controladores` para expor a API.

---

### Complexidade: O Grande Inimigo
* O software tende a se tornar complexo porque os problemas que ele resolve são complexos.
* A complexidade aumenta a chance de erros, dificulta a manutenção e a colaboração.
* A **Orientação a Objetos (OO)** é a principal estratégia para gerenciar essa complexidade, permitindo decompor um problema grande em partes menores e mais gerenciáveis.

---

### Orientação a Objetos e Frameworks
* **Orientação a Objetos (OO):** É um paradigma essencial. O objetivo é aprender a modelar qualquer parte de um sistema (dados, lógica, interfaces) como objetos, que possuem atributos (informações) e métodos (ações).
* **Padrões de Código:** Adotar padrões de nomenclatura e estilo de código (ex: Camel Case em Java) é crucial para a legibilidade e manutenção do projeto.
* **Frameworks (`Spring Boot`, `ASP.NET`, etc.):** O uso de frameworks é uma boa prática para não "reinventar a roda". Eles fornecem uma estrutura testada e soluções para problemas comuns, permitindo que o desenvolvedor foque na lógica de negócio.

---

### Princípios de uma Boa Arquitetura

* **Ocultamento de Informação (Encapsulamento):**
    * Assim como não precisamos entender de eletrônica para usar um videogame, os componentes de um software devem esconder sua complexidade interna.
    * Isso é alcançado com o uso de **classes**, que expõem interfaces simples (`public`) e escondem os detalhes da implementação (`private`).

* **Baixo Acoplamento e Flexibilidade para Mudanças:**
    * Um dos objetivos mais importantes é criar um código **desacoplado**, onde as partes do sistema não dependem diretamente umas das outras.
    * Isso foi exemplificado pela arquitetura usada em Fábrica de Software: o `Controller` não conhece a implementação do `Service`, mas sim a sua **interface**.
    * Essa abordagem permite que a implementação (`ServiceImpl`) seja alterada ou substituída sem quebrar o código que a utiliza, tornando o sistema mais flexível e fácil de manter.

---

### Decisões Arquiteturais
* A escolha da tecnologia (linguagem, framework) é uma das decisões mais críticas e difíceis.
* Foi apresentado o conceito de **"Estradas Pavimentadas"** (usado por empresas como Netflix e Conta Azul): a empresa oferece um conjunto de tecnologias recomendadas e com suporte. As equipes têm autonomia para usar outras tecnologias, mas assumem a responsabilidade total por elas.

---



## Próximos Estudos
- Arquitetura de software e atributos de qualidade.  
- Capítulo 1 do livro *Engenharia de Software Moderna*. 

 
- Relacionar teoria com prática em **Java + Angular**.  

# Aula 02- 04/08/2025

A aula iniciou com uma revisão dos conceitos anteriores, como **ocultamento de informação**, a importância do desenvolvimento paralelo e a busca por flexibilidade e compreensibilidade no código através da **Orientação a Objetos (OO)**.

## Tópicos Principais

### Encapsulamento e Getters/Setters
* O encapsulamento é a técnica usada para implementar o ocultamento de informação na prática.
* `Getters` e `setters` são a manifestação desse princípio, protegendo os dados (`private`) de uma classe e controlando o acesso a eles.

---

### Coesão (Alta Coesão)
* **Definição:** É o princípio de que uma classe ou método deve ter uma **única responsabilidade** bem definida. O objetivo é criar componentes que fazem uma coisa só, e a fazem bem.
* **Benefícios:** Um código com alta coesão é mais fácil de entender, testar e manter. Evita a criação de classes "faz-tudo" que se tornam difíceis de gerenciar com o tempo.

---

### Acoplamento (Baixo Acoplamento)
* **Definição:** Refere-se ao nível de dependência entre diferentes partes de um sistema. O ideal é ter um **baixo acoplamento**, onde a alteração em um componente não quebra outros.
* **Exemplos Práticos:**
    * **Forte Acoplamento:** Uma classe que instancia e chama métodos de outra classe diretamente.
    * **Baixo Acoplamento:** Utilizar **interfaces** para a comunicação. O código depende do "contrato" (a interface), e não da implementação concreta. Isso foi exemplificado com o uso de `@Autowired` no Spring e a abstração do banco de dados com o Spring Data JPA, que permite trocar a implementação sem quebrar o sistema.

---

### Introdução aos Princípios SOLID
* SOLID é um acrônimo para cinco princípios de design de software que ajudam a criar sistemas mais compreensíveis, flexíveis e manuteníveis.
* O primeiro princípio, **"S" - Single Responsibility Principle (Princípio da Responsabilidade Única)**, é a aplicação direta do conceito de **alta coesão**.

# Aula 03 - 07/08/2025

A aula iniciou com a revisão dos conceitos de **alta coesão** e **baixo acoplamento** como objetivos centrais na construção de software. O foco principal foi a introdução e o aprofundamento nos dois primeiros princípios do **SOLID**.

## Tópicos Principais

### Introdução ao SOLID
* SOLID é um acrônimo para cinco princípios de design para software orientado a objetos, popularizados por **Robert Martin (Uncle Bob)**.
* Seguir estes princípios ajuda a criar um código mais limpo, manutenível e flexível. Em resumo, é "programar orientado a objetos do jeito certo".

---

### S - Princípio da Responsabilidade Única (SRP)
* Este princípio é a aplicação direta do conceito de **alta coesão**.
* Afirma que uma classe deve ter apenas **um, e somente um, motivo para mudar**.
* A arquitetura em camadas utilizada anteriormente (`entity`, `service`, `controller`) é um exemplo prático, onde cada camada possui uma responsabilidade clara e única.

---

### I - Princípio da Segregação de Interfaces (ISP)
* O princípio defende que é melhor ter **várias interfaces pequenas e específicas** do que uma única interface grande e genérica.
* O objetivo é evitar que uma classe seja obrigada a implementar métodos que ela não utiliza.
* **Exemplo prático:** Em vez de uma única interface para todos os eventos de UI, foram usadas interfaces segregadas:
    * `ActionListener`: Exclusiva para tratar eventos de clique.
    * `MouseMotionListener`: Exclusiva para tratar eventos de movimento do mouse.

---

### Aplicando os Princípios em Conjunto
* Foi demonstrado que, embora o uso de interfaces separadas atendesse ao **ISP**, a classe da Janela (`JFrame`) passou a ter múltiplas responsabilidades (desenhar a tela e tratar a lógica dos eventos), violando o **SRP**.
* A solução foi refatorar o código, criando uma classe `Controlador` separada para conter a lógica e implementar as interfaces.
* **Resultado Final:**
    * A classe `Janelinha` ficou apenas com a responsabilidade de montar e exibir a interface.
    * A classe `Controlador` ficou com a responsabilidade de gerenciar a lógica dos eventos, respeitando ambos os princípios.

# Aula 4- 11/08/2025

Esta aula concluiu o estudo dos **Princípios SOLID**, focando nos três pilares restantes: Inversão de Dependência, Substituição de Liskov e o Princípio do Aberto/Fechado.

## Tópicos Principais

### D - Princípio da Inversão de Dependência (DIP)
* **Definição:** Componentes devem depender de **abstrações (interfaces)**, e não de implementações concretas.
* **Na prática:** Isso desacopla o código. Em vez de um `Controller` conhecer o `ServiceImpl`, ele conhece apenas a interface `Service`. A implementação real é "injetada" em tempo de execução (ex: via `@Autowired` no Spring), permitindo que ela seja trocada sem quebrar o `Controller`.

---

### L - Princípio da Substituição de Liskov (LSP)
* O tópico foi abordado sob a ótica de **"Prefira Composição à Herança"**.
* **Herança:** Deve ser usada com cautela. Ela cria um forte acoplamento e pode ser difícil de modelar em bancos de dados. Use-a apenas quando as subclasses são totalmente distintas (a analogia "gato e cachorro").
* **Composição/Associação:** É uma alternativa mais flexível, permitindo que objetos colaborem sem criar uma hierarquia rígida, resultando em um design mais robusto.

---

### O - Princípio do Aberto/Fechado (OCP)
* **Definição:** O software deve ser **aberto para extensão, mas fechado para modificação**.
* **Na prática:** É possível adicionar novas funcionalidades a uma classe sem alterar seu código-fonte.
* **Exemplo:** A customização de um `JTable` foi usada para ilustrar o conceito. Não modificamos a classe `JTable`. Em vez disso, **estendemos** seu comportamento ao fornecer uma implementação de `AbstractTableModel`, adicionando a lógica de exibição de dados de forma segura e desacoplada.

# Aula 5- 14/08/2025

Esta aula concluiu o estudo dos **Princípios SOLID**, com foco no último princípio: a Substituição de Liskov.

## Tópicos Principais

### Revisão dos Princípios Anteriores
* A aula começou com uma rápida recapitulação dos princípios já vistos:
    * **Inversão de Dependência (DIP):** Depender de abstrações (interfaces).
    * **Composição sobre Herança:** Dar preferência a associações em vez de herança.
    * **Lei de Demeter (LoD):** Limitar o conhecimento que um objeto tem sobre outros.
    * **Aberto/Fechado (OCP):** Ser aberto para extensão, mas fechado para modificação.

---

### L - Princípio da Substituição de Liskov (LSP)
* **Definição:** Este é o último princípio do acrônimo SOLID. Ele estabelece que objetos de uma superclasse devem ser substituíveis por objetos de suas subclasses sem afetar a integridade do programa.
* **Na prática:** As classes filhas devem honrar o contrato estabelecido pela classe pai, mantendo a assinatura e o comportamento esperado dos métodos herdados. Isso garante que diferentes implementações de uma mesma abstração sejam intercambiáveis.
* **Exemplo Prático (Java Swing):**
    * Um `JPanel` foi criado para receber uma borda.
    * Primeiro, foi aplicada uma `LineBorder`. O programa funcionou.
    * Em seguida, a `LineBorder` foi substituída por uma `TitledBorder`. O programa continuou funcionando sem nenhuma alteração.
    * **Conclusão:** Isso foi possível porque tanto `LineBorder` quanto `TitledBorder` herdam da mesma classe base (`AbstractBorder`) e respeitam seu contrato. Elas são, portanto, substituíveis entre si, demonstrando o LSP na prática.

---

### Conclusão sobre SOLID
* Com a exploração do LSP, finalizamos o estudo dos cinco princípios SOLID. Uma arquitetura de software robusta e manutenível deve se esforçar para aplicar esses conceitos.

# Aula 6- 18/08/2025

Após uma breve revisão do Princípio da Substituição de Liskov (LSP), a aula introduziu o conceito de **Padrões de Projeto (Design Patterns)** e implementou o primeiro deles: o Singleton.

## Tópicos Principais

### Introdução aos Padrões de Projeto
* **Definição:** São soluções padronizadas para problemas recorrentes no design de software orientado a objetos.
* **Objetivo:** Reutilizar soluções comprovadas para aumentar a flexibilidade e a manutenibilidade do código.
* **Categorias:** Criacionais, Estruturais e Comportamentais.

---

### Padrão Criacional: Singleton
* **Intenção:** Garantir que uma classe tenha **uma, e somente uma, instância**, e fornecer um ponto de acesso global para ela.

* **Implementação Chave:**
    * **Construtor Privado:** `private Singleton()`
        * Impede a instanciação da classe através do operador `new` por qualquer código externo.
    * **Instância Estática Privada:** `private static Singleton instance;`
        * Cria uma única variável que pertence à classe em si, não a um objeto individual. É o "recipiente" para a instância única.
    * **Método de Acesso Estático Público:** `public static Singleton getInstance()`
        * É a única forma de obter a instância da classe.
        * Na primeira chamada, ele cria o objeto (`new Singleton()`) e o armazena na variável estática.
        * Nas chamadas seguintes, ele simplesmente retorna a instância já criada, garantindo que ela seja sempre a mesma.

* **Uso e Advertência:**
    * O Singleton é útil para gerenciar recursos compartilhados (ex: configurações, pools de conexão).
    * No entanto, é frequentemente considerado um **anti-padrão**, pois cria um estado global que pode levar a um alto acoplamento no sistema e dificultar a realização de testes unitários. Deve ser usado com moderação.

# Aula 7- 21/08/2025

Esta aula consistiu em uma revisão prática e aprofundada do padrão **Singleton**, incluindo uma sessão de debugging para visualizar seu funcionamento, e a introdução de um novo desafio de implementação.

## Tópicos Principais

### Revisão e Analogia do Padrão Singleton
* **Objetivo Principal:** Garantir que uma classe possua apenas **uma instância** em toda a aplicação.
* **Analogia "Ender Chest":** O Singleton foi comparado a um "Ender Chest" do Minecraft. Não importa onde você o acesse no sistema, você sempre estará interagindo com o mesmo objeto e os mesmos dados.
* **Pilares da Implementação:**
    * `private constructor()`: Bloqueia a criação de instâncias externas.
    * `private static Singleton instance`: Uma variável estática para guardar a única instância.
    * `public static getInstance()`: Método de acesso que cria a instância apenas na primeira vez e a retorna em todas as chamadas subsequentes.

---

### Demonstração Prática e Debugging
* Para dar um propósito ao Singleton, uma variável `segredo` foi adicionada para guardar uma informação.
* Uma classe `Cliente` demonstrou o fluxo de uso:
    1.  Obter a instância com `Singleton.getInstance()`.
    2.  Salvar uma informação: `singleton.setSegredo(...)`.
    3.  Em outro ponto do sistema, obter a instância novamente e recuperar a informação: `Singleton.getInstance().getSegredo()`.
* Foi realizada uma sessão de **debugging** para executar o código passo a passo, mostrando como as variáveis são preenchidas na memória e provando que a instância do Singleton e a informação guardada nela permanecem as mesmas durante a execução.

---

### Novo Desafio: O Padrão Observer
* A próxima tarefa para a turma é implementar o padrão de projeto **Observer** de forma autônoma.
* O objetivo é praticar a habilidade de analisar um diagrama UML de um padrão e traduzir sua estrutura e lógica para código funcional.
