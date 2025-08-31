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

### 1. Abstração: A Essência do Software
* O principal trabalho no desenvolvimento de software é a **abstração**: entender um problema do mundo real e representá-lo em código.
* Exemplos práticos do projeto anterior (Fábrica de Software) foram citados, como a criação de `Entidades` para representar dados, `Repositórios` para abstrair o acesso ao banco de dados, `Serviços` para a lógica de negócio e `Controladores` para expor a API.

### 2. Complexidade: O Grande Inimigo
* O software tende a se tornar complexo porque os problemas que ele resolve são complexos.
* A complexidade aumenta a chance de erros, dificulta a manutenção e a colaboração.
* A **Orientação a Objetos (OO)** é a principal estratégia para gerenciar essa complexidade, permitindo decompor um problema grande em partes menores e mais gerenciáveis.

### 3. Orientação a Objetos e Frameworks
* **Orientação a Objetos (OO):** É um paradigma essencial. O objetivo é aprender a modelar qualquer parte de um sistema (dados, lógica, interfaces) como objetos, que possuem atributos (informações) e métodos (ações).
* **Padrões de Código:** Adotar padrões de nomenclatura e estilo de código (ex: Camel Case em Java) é crucial para a legibilidade e manutenção do projeto.
* **Frameworks (`Spring Boot`, `ASP.NET`, etc.):** O uso de frameworks é uma boa prática para não "reinventar a roda". Eles fornecem uma estrutura testada e soluções para problemas comuns, permitindo que o desenvolvedor foque na lógica de negócio.

### 4. Princípios de uma Boa Arquitetura

* **Ocultamento de Informação (Encapsulamento):**
    * Assim como não precisamos entender de eletrônica para usar um videogame, os componentes de um software devem esconder sua complexidade interna.
    * Isso é alcançado com o uso de **classes**, que expõem interfaces simples (`public`) e escondem os detalhes da implementação (`private`).

* **Baixo Acoplamento e Flexibilidade para Mudanças:**
    * Um dos objetivos mais importantes é criar um código **desacoplado**, onde as partes do sistema não dependem diretamente umas das outras.
    * Isso foi exemplificado pela arquitetura usada em Fábrica de Software: o `Controller` não conhece a implementação do `Service`, mas sim a sua **interface**.
    * Essa abordagem permite que a implementação (`ServiceImpl`) seja alterada ou substituída sem quebrar o código que a utiliza, tornando o sistema mais flexível e fácil de manter.

### 5. Decisões Arquiteturais
* A escolha da tecnologia (linguagem, framework) é uma das decisões mais críticas e difíceis.
* Foi apresentado o conceito de **"Estradas Pavimentadas"** (usado por empresas como Netflix e Conta Azul): a empresa oferece um conjunto de tecnologias recomendadas e com suporte. As equipes têm autonomia para usar outras tecnologias, mas assumem a responsabilidade total por elas.

## Próximos Estudos
- Arquitetura de software e atributos de qualidade.  
- Capítulo 1 do livro *Engenharia de Software Moderna*. 

 
- Relacionar teoria com prática em **Java + Angular**.  
