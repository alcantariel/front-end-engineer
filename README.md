# Arquitetura e Design

## Arquitetura

É o processo de conversão de características como, flexibilidade, escalabilidade, resiliência, viabilidade, reutilização e segurança, que atenda as expectativas técnicas e principalmente de negócios/operacionais.

É responsável pelo esqueleto e infraestrutura de alto nível.

<br>

## Design

É responsável pelo design no nível de código, como, o que cada módulo está fazendo, escopo de classes e funções.

- clean code
- princípios de desenvolvimento
- padrões de projeto

<br>

## Características da Arquitetura de Software

### Extensível

Qualidade de ser projetado para permitir a adição de novos recursos ou funcionalidades, ou seja, ser personalizável. Ex: adição de plugins ou addons.

<br>

### Modular

É a decomposição em partes menores com interfaces padronizadas, ou seja, um módulo é um pedaço de código que pode ser reutilizado e combinado com outros módulos, ou até mesmo substituído.

<br>

### Interoperabilidade

É responsável pela sua operação e transmissão/troca de dados com outros sistemas externos. Para melhoras a interoperabilidade, é possível utilizar interfaces externas, sistemasa de padronização, etc.

<br>

### Sustentável

Com sustentável, pode se dizer que o software deve ser eficiente. Que fará a utilização dos recursos da melhor forma, levando em consideração o que tem disponível para execução.

<br>

### Performance

Resposta do sistema com base na execução de determinadas ações por um determinado período de tempo.

Maneiras de medir o desempenho:

- Latência: tempo gasto na resposta a um evento
- Capacidade do Canal: número de eventos que ocorrem em um determinado ponto no tempo

Quanto menor a latência, maior a performance...

<br>

### Escalabilidade

É a capacidade do sistema lidar com o aumento de carga sem d iminuir o desempenho, ou é a possibilidade de aumentar a carga de forma rápida.

Existem duas maneiras de melhorar a escalabilidade:

- Vertical (RECURSO): para aumentar, é necessário adicionar mais recursos, como memória, discos ou processadores de uma máquina/sistema
- Horizontal (UNIDADES): para aumentar, é necessário adicionar mais unidades de computação e dividir a carga entre elas

<br>

### Tolerância a Falhas

Refere-se a capacidade de um sistema continuar operando sem interrupção quando um ou mais de seus componentes falham, garantindo alta diponibilidade e continuidade de negócios. Sistemas tolerantes a falhas, utilizam componentes de backup, que substituem automaticamente os componentes com falha para que não haja perda de serviço.

<br>

### Segurança

É responsável pela capacidade do sistema reduzir a probabilidade de ações maliciosas ou acidentais, assim como a probabilidade de roubo ou perda de informações.

<br>

### Confiabilidade

É um atributo responsável pela capacidade de continuar operando sob condições predefinidas. Na maioria das vezes o sistema falha devido à inacessibilidade de elementos externos.

<br>

### Resiliência

É a capacidade de fornecer e manter um nível aceitável de serviço diante das falhas e desafios. Estas falhas podem variar de uma simples configuração incorreta, até grandes desastres naturais.

<br>

## Padrões de Arquitetura de Software

Disponibilidade ou modelo dos recursos/componentes disponíveis, assim como o relacionamento entre estes a fim de resolver um problema.

<br>

### Serverless

Refere-se a uma solução que depende de serviços de terceiros para gerenciar a complexidade dos servidores e o gerenciamento backend.

A arquitetura Serverless é dividida em duas categorias:

- backend como serviço (BaaS)
- funções como serviço (FaaS)

Ajuda a economizar tempo, já que não tem um backend para implementar, corrigir bugs ou fazer tarefas regulares de servidores.

O serviço mais famoso atualmente é o AWS Lambda.

![Serverless](./assets/serverless.png)

<br>

### Event-driven

Depende de **Produtores de Eventos** e **Consumidores de Eventos**.

A ideia é desacoplar as partes do sistema onde cada parte será acionada quando um evento é produzido.

Eventos produtores são dependentes de alguma ação do usuário/tempo para ser produzido.

Os sistemas consumidores ficam escutando a eventos com base em um "tipo".

![Event Driven](./assets/event-driven.png)

<br>

### Microsserviços

Depende do desenvolvimento de pequenos serviços ou módulos, que são independentes, onde, cada serviço/módulo resolve um problema específico ou executa uma única tarefa.

Esses módulos comunicam entre si por meio de uma API definida para atender o objetivo do negócio.

![Microservices](./assets/microservices.png)

<br>

## Princípios de Desenvolvimento

### SOLID

- **S**ingle Responsability: significa que cada classe deve ter um único propósito, uma responsabilidade e um motivo para mudar.

- **O**pen Closed: signiica que uma classe deve estar aberta para extensão e fechada para modificação. Em outras palavras, deve ser possível adicionar mais funcionalidades na classe, mas sem editar as funções atuais de uma forma que interrompa o código existente e que a utiliza.

- **L**iskov Substitution: orienta o desenvolvedor a utilizar herança de uma maneira que uma classe filha "B" herdar de uma classe pai "A", a classe filha não deve replicar uma funcionalidade da classe pai de forma a alterar o comportamento da classe pai. Assim elas se tornam independentes e não quebram a lógica da aplicação.

- **I**nterface Segregation: como uma classe pode implementar múltiplas interfaces, o código deve ser estruturado de uma forma que uma classe nunca seja forçada a implementar uma função que não seja importante para seu propósito.

- **D**ependency Inversion: se uma determinada classe "Purchase" depende da classe "User", então a instanciação do objeto User deve vir de fora da classe Purchase. A abstração não depende do detalhe, o detalhe que depende da abstração.

<br>

## Referências

https://github.com/donnemartin/system-design-primer#performance-vs-scalability

https://codeburst.io/software-architecture-the-difference-between-architecture-and-design-7936abdd5830

https://medium.com/storyblocks-engineering/web-architecture-101-a3224e126947

https://hackernoon.com/quality-attributes-in-software-architecture-3844ea482732
