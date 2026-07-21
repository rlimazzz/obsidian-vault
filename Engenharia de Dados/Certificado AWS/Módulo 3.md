## AWS Compute Options

A AWS oferece serviços gerenciados e não gerenciados para atender a diferentes níveis de controle e responsabilidade. Ao entender esse modelo, você saberá quais são tarefas que a AWS gerencia e quais são as tarefas pelais quais você é responsável, o que ajuda a proteger e gerenciar os recursos de nuvem de forma eficaz.

Serverless: É um modelo de nuvem onde o provedor gerencia a infraestrutura. Você executa os códigos sem provisionar ou gerenciar a servidores. A plataforma escala automaticamente e você paga apenas pelos recursos consumidos durante a execução.

Com serviços não gerenciados como a solução Amazon EC2, você configura e gerencia tudo: o sistema operacional, as atualizações de segurança e as configurações de rede. A AWS cuida apenas do hardware físico. Os serviços gerenciados lidam com a maior parte da infraestrutura, mas você ainda precisa configurar coisas como opções de implantação, scaling e configurações do ambiente. Com serviços totalmente gerenciados, como a solução AWS Lambda, você não gerencia nenhum servidor. Você carrega seu código e a AWS cuida do resto, inclusive infraestrutura, escalabilidade e disponibilidade.

A solução Lambda é um serviço computacional sem servidor que executa código em resposta a eventos sem a necessidade de provisionar ou gerenciar servidores. Ela gerencia de forma automática a infraestrutura subjacente para escalar os recursos de acordo com o volume de solicitações. A cobrança é feita de acordo com o tempo computacional consumido, até o milissegundo. A solução Lambda lida com execução, scaling e alocação de recursos. É possível otimizar o desempenho ao configurar o tamanho de memória apropriado para sua função.

Embora a AWS gerencie a infraestrutura, a equipe é responsável por configurar corretamente as funções e permissões da solução AWS Identity and Access Management (IAM) para qualquer serviço que a função Lambda acesse.

Os principais componentes da solução AWS Lambda são a função, os gatilhos e os runtimes. Esses componentes manipulam o código, respondem a eventos e fornecem o ambiente de linguagem. Os clientes não precisam gerenciar servidores, scaling ou sistemas operacionais. A AWS cuida de tudo isso.

## Contêineres

[[Básicos]]

Um contêiner empacota sua aplicação com tudo o que ela precisa para ser executada, para que funcione da mesma forma em qualquer computador. Isso ajuda a mover, atualizar e gerenciar. Os contêineres são mais rápidos e leves do que as máquinas virtuais (VMs) porque compartilham o sistema operacional do computador host. As VMs usam um hipervisor para executar sistemas operacionais completos e separados, o que as torna menos eficientes em termos de recursos, além de terem tempos de inicialização mais longos.

À medida que as aplicações em contêineres se expandem, o gerenciamento se torna mais complexo. Uma configuração que começou com alguns contêineres em um único host pode crescer de forma rápida para centenas ou milhares de contêineres em vários hosts. Nessa escala, o manuseio manual do ciclo de vida do contêiner, o monitoramento e as operações gerais tornam-se insustentáveis. É aqui que entram as ferramentas de orquestração. Elas automatizam a implantação, o dimensionamento e o gerenciamento para manter o pleno funcionamento de tudo.

A solução Amazon Elastic Container Service (Amazon ECS) é um serviço escalável de orquestração de contêineres que executa e gerencia contêineres na AWS, como contêineres Docker. O Docker é uma plataforma de software para criar, testar e implantar aplicações de forma rápida.

A solução Amazon Elastic Kubernetes Service (Amazon EKS) é um serviço totalmente gerenciado para executar o Kubernetes na AWS. Ela simplifica a implantação, o gerenciamento e o escalonamento de aplicações em contêineres com o uso do Kubernetes de código aberto, com suporte e atualizações contínuos da comunidade em geral.

A solução Amazon Elastic Container Registry (Amazon ECR) é onde é possível armazenar, gerenciar e implantar imagens de contêineres. Ela é compatível com imagens de contêiner que seguem os padrões da Open Container Initiative (OCI). É possível enviar, extrair e gerenciar imagens em seus repositórios da solução Amazon ECR com o uso de ferramentas de contêiner padrão e interfaces de linha de comando (CLIs).

A solução AWS Fargate é um mecanismo computacional sem servidor para contêineres. Ela funciona com as soluções Amazon ECS e Amazon EKS. A solução Fargate é uma plataforma de hospedagem de contêineres, ao contrário das soluções Amazon ECS e Amazon EKS, sendo que ambas são serviços de orquestração de contêineres.

Ao usar a solução Fargate, não é preciso provisionar ou gerenciar servidores. A solução Fargate gerencia a infraestrutura de servidor para você. É possível se concentrar em inovar e desenvolver suas aplicações e pagar apenas pelos recursos necessários para executar os contêineres.

A solução Amazon ECS é um serviço escalável para orquestrar contêineres na AWS, enquanto a solução Amazon EKS ajuda a simplificar a implantação do Kubernetes. A solução Amazon ECR armazena e gerencia imagens de contêineres compatíveis com OCI para se integrar às soluções Amazon ECS, Amazon EKS e Fargate. A solução Fargate é um mecanismo de computacional sem servidor para contêineres que elimina a necessidade de gerenciar a infraestrutura para trabalhar com as soluções Amazon ECS e Amazon EKS.