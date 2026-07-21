## AWS Compute Options

A AWS oferece serviços gerenciados e não gerenciados para atender a diferentes níveis de controle e responsabilidade. Ao entender esse modelo, você saberá quais são tarefas que a AWS gerencia e quais são as tarefas pelais quais você é responsável, o que ajuda a proteger e gerenciar os recursos de nuvem de forma eficaz.

Serverless: É um modelo de nuvem onde o provedor gerencia a infraestrutura. Você executa os códigos sem provisionar ou gerenciar a servidores. A plataforma escala automaticamente e você paga apenas pelos recursos consumidos durante a execução.

Com serviços não gerenciados como a solução Amazon EC2, você configura e gerencia tudo: o sistema operacional, as atualizações de segurança e as configurações de rede. A AWS cuida apenas do hardware físico. Os serviços gerenciados lidam com a maior parte da infraestrutura, mas você ainda precisa configurar coisas como opções de implantação, scaling e configurações do ambiente. Com serviços totalmente gerenciados, como a solução AWS Lambda, você não gerencia nenhum servidor. Você carrega seu código e a AWS cuida do resto, inclusive infraestrutura, escalabilidade e disponibilidade.

A solução Lambda é um serviço computacional sem servidor que executa código em resposta a eventos sem a necessidade de provisionar ou gerenciar servidores. Ela gerencia de forma automática a infraestrutura subjacente para escalar os recursos de acordo com o volume de solicitações. A cobrança é feita de acordo com o tempo computacional consumido, até o milissegundo. A solução Lambda lida com execução, scaling e alocação de recursos. É possível otimizar o desempenho ao configurar o tamanho de memória apropriado para sua função.

Embora a AWS gerencie a infraestrutura, a equipe é responsável por configurar corretamente as funções e permissões da solução AWS Identity and Access Management (IAM) para qualquer serviço que a função Lambda acesse.

Os principais componentes da solução AWS Lambda são a função, os gatilhos e os runtimes. Esses componentes manipulam o código, respondem a eventos e fornecem o ambiente de linguagem. Os clientes não precisam gerenciar servidores, scaling ou sistemas operacionais. A AWS cuida de tudo isso.