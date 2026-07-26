O treinamento de ML produz um modelo que pode ser aplicado a novos dados para fazer previsões ou decisões com base nos padrões aprendidos.

A Inteligência Artificial é um campo amplo focado no desenvolvimento de sistemas computacionais inteligentes capazes de realizar tarefas semelhantes às humanas.

O machine learning é um tipo de IA para treinar máquinas a realizar tarefas complexas sem instruções explícitas. O treinamento de machine learning encontra os padrões ocultos em grandes quantidades de dados históricos para produzir um modelo de ML. Esse modelo de ML pode então ser aplicado a novos dados para fazer previsões ou decisões com base nos padrões aprendidos.

A pilha de IA/ML da AWS é composta pelos seguintes três níveis de soluções:

- _Serviços de IA_ — modelos pré-construídos que já são treinados para executar funções específicas
    
- _Serviços de ML_ — uma abordagem mais personalizada com o Amazon SageMaker AI, na qual você cria, treina e implanta seus próprios modelos de ML com infraestrutura totalmente gerenciada
    
- _Frameworks e infraestrutura de ML_ — uma abordagem totalmente personalizada para criar modelos usando chips criados para fins específicos que se integram a frameworks de ML populares

O Amazon Comprehend pode extrair informações importantes, como a opinião do cliente, dos documentos. Isso pode ajudar a proprietária a entender melhor seus clientes.

Com o Amazon Lex, a empresa pode adicionar interfaces de conversação de voz e texto às suas aplicações para criar conversas realistas. Ele pode aprimorar a aplicação de suporte ao cliente da empresa de saúde.

O Amazon Polly converte texto em fala realista. Ele suporta vários idiomas, gêneros diferentes e uma variedade de sotaques. É a combinação ideal para esse caso de uso.

Eles podem usar a IA do SageMaker para desenvolver seus modelos de ML sem se preocupar com a infraestrutura. Os data scientists podem usar o IDE e os analistas de negócios podem usar a interface sem código.

O aprendizado profundo (DL) é um subconjunto do machine learning em que os modelos são treinados usando camadas de neurônios artificiais que imitam o cérebro humano. Cada camada dessas redes neurais resume e envia informações para a próxima camada até que um modelo final seja produzido.

A IA generativa é um tipo de aprendizado profundo alimentado por modelos de ML extremamente grandes, conhecidos como modelos de base (FMs). Os FMs são pré-treinados em vastas coleções de dados. Enquanto os modelos tradicionais de ML são treinados para realizar tarefas singulares, os FMs podem ser adaptados para realizar várias tarefas.

A AWS oferece os seguintes tipos de soluções de IA generativa:

- _Amazon SageMaker JumpStart_—Um hub de ML com FMs e soluções de ML pré-criadas que podem ser implantadas com alguns cliques
    
- _Amazon Bedrock_—Um serviço totalmente gerenciado para adaptar e implantar FMs da Amazon e de outras empresas líderes em IA
    
- _Amazon Q_—Um assistente de IA interativo que pode ser integrado aos repositórios de informações de uma empresa

O Amazon SageMaker Jumpstart oferece implantação rápida de soluções de ML. No entanto, outro serviço pode ser melhor para uma IA generativa multimodal totalmente gerenciada e de nível empresarial.

O Amazon Bedrock funcionaria bem para uma IA generativa multimodal totalmente gerenciada, de nível empresarial.

O Amazon Q Developer fornece recomendações de código para acelerar o desenvolvimento de aplicações em C#, Java, JavaScript, Python e TypeScript. É uma boa opção para esse caso de uso.


Tanto a IA/ML quanto a data analytics tradicional precisam de dados limpos e acessíveis em um formato que possa ser usado por ferramentas de análise e algoritmos de IA. Os processos de ETL são usados para essa finalidade. Com o ETL, você executa as seguintes etapas:

1. _Extraia_ os dados de várias origens e armazene-os.
    
2. _Transforme-o_ em um formato consistente e utilizável para o consumo de ferramentas posteriores.
    
3. _Carregue-o_ em um sistema de destino, como um data warehouse ou uma plataforma de análise.
    

Os pipelines de dados são linhas de montagem automatizadas usadas para tornar o processo ETL eficiente e repetível. A AWS tem um pacote de serviços integrados para que você possa criar seus próprios pipelines de dados.

> **Amazon Kinesis Data Streams**

Você pode usar o Kinesis Data Streams para a ingestão em tempo real de terabytes de dados de aplicações, streams e sensores. Esse serviço com tecnologia sem servidor fornece até mesmo provisionamento e scaling automáticos no modo sob demanda.

> **Amazon Data Firehose**

O Firehose é uma opção para ingestão de dados quase em tempo real. Esse serviço totalmente gerenciado fornece provisionamento e scaling automáticos. Ele também entrega dados em segundos para data lakes, armazéns e serviços de análise.

### Serviços de armazenamento de dados

> **Amazon S3**

O Amazon S3 é uma escolha popular para data lakes. Esse serviço de armazenamento de objetos pode armazenar com segurança praticamente qualquer quantidade de dados estruturados ou não estruturados. O Amazon S3 também é totalmente elástico, com auto scaling à medida que você adiciona e remove dados.

> **Amazon Redshift**

O Amazon Redshift é um serviço de data warehouse totalmente gerenciado que pode armazenar petabytes de dados estruturados ou semiestruturados. Com a escalabilidade e o modelo de preços com pagamento conforme o uso, as organizações podem analisar grandes conjuntos de dados de forma econômica.

### Serviços de catalogação de dados

> **AWS Glue Data Catalog**

O AWS Glue Data Catalog fornece um repositório de metadados centralizado, dimensionável e gerenciado que aprimora a descoberta de dados. Ele melhora a eficiência geral dos pipelines de dados ao fornecer metadados para vários armazenamentos de dados e serviços de análise.

### Serviços de processamento de dados

> **AWS Glue**

O AWS Glue é um serviço de ETL totalmente gerenciado que torna a preparação de dados mais simples, rápida e econômica. Os trabalhos de ETL do AWS Glue podem usar o catálogo de dados do AWS Glue para acessar metadados sobre fontes de dados, o que pode ajudar a informar as transformações definidas no script ETL.

> **Amazon EMR**

O Amazon EMR é ideal para processamento de dados em grande escala e organizações com experiência existente em big data. Ele gerencia automaticamente o provisionamento da infraestrutura, o gerenciamento de clusters e scaling. O Amazon EMR oferece suporte a frameworks populares de big data, como Apache Spark, Apache Hadoop e Apache Hive.

### Serviços de análise e visualização de dados

> **Amazon Athena**

Com o Athena, você pode executar consultas SQL para analisar dados em fontes de dados relacionais, não relacionais, de objetos e personalizadas. Esse serviço com tecnologia sem servidor totalmente gerenciado pode acessar dados hospedados no Amazon S3, on-premises ou até mesmo em ambientes multinuvem. Ele oferece uma solução econômica para análise de dados, pois você paga apenas pelas consultas executadas.

> **Amazon Redshift**

O Amazon Redshift é uma solução de data warehouse totalmente gerenciada. Seu armazenamento em colunas e sua arquitetura de processamento massivamente paralelo o tornam ideal para analisar grandes conjuntos de dados. Você pode usá-lo para realizar consultas SQL complexas em grandes conjuntos de dados para workloads analíticas frequentes e de alto desempenho.

> **Amazon QuickSight**

Com o QuickSight, usuários técnicos e não técnicos podem criar rapidamente painéis e relatórios interativos modernos a partir de várias fontes de dados sem gerenciar a infraestrutura. O Amazon Q no QuickSight fornece consultas em linguagem natural para que analistas de negócios e usuários possam criar, descobrir e compartilhar informações significativas em segundos.

> **Amazon OpenSearch Service**

Com o OpenSearch Service, você pode pesquisar conteúdo relevante por meio de correspondência precisa de palavras-chave ou consultas em linguagem natural. Os painéis unificados fornecem visualização de dados em tempo real à medida que você analisa e monitora logs, rastreamentos e métricas de várias aplicações.