### Bancos de Dados Relacionais

Os bancos de dados relacionais armazenam dados de forma a relacioná-los com outros dados, e usam a linguagem de consulta estruturada, ou SQL, para gerenciar e consultar dados. Essa abordagem armazena dados de uma forma facilmente compreensível, consistente e dimensionável, que funciona muito bem para aplicações que exigem gerenciamento estruturado de dados.

A soluçãoAmazon RDS é um serviço de banco de dados relacional _gerenciado_ que lida com tarefas rotineiras de banco de dados, como backups, patches e provisionamento de hardware. A solução Amazon RDS oferece suporte a vários tipos de classes de instâncias de banco de dados que otimizam memória, desempenho ou entrada/saída (E/S).

Para melhorar a resiliência dos dados, a solução Amazon RDS oferece implantação Multi-AZ e backups automatizados, mas também é possível criar backups de forma manual com o uso de snapshots de banco de dados. Esses são backups completos de toda a instância do banco de dados, que podem ser úteis para fins específicos de recuperação pontual ou arquivamento de dados de longo prazo. A solução Amazon RDS oferece atributos de segurança, inclusive isolamento de rede, criptografia em trânsito e criptografia em repouso. É possível escalar de forma fácil os recursos do banco de dados vertical ou horizontalmente, conforme necessário.

O Aurora é um banco de dados relacional gerenciado e projetado para ajudar a reduzir operações de E/S desnecessárias. Ele é compatível com MySQL e PostgreSQL, oferece alto desempenho e disponibilidade, além de se adaptar de forma automática às workloads. O Aurora replica dados em várias Zona de Disponibilidade para maior durabilidade e tolerância a falhas, além de oferecer atributos de backups automatizados, criptografia em repouso e monitoramento contínuo.

A arquitetura de armazenamento distribuído Aurora oferece até cinco vezes o throughput do MySQL padrão enquanto mantém a compatibilidade. Ele foi projetado de forma específica para lidar com altas workloads de transações e distribuir E/S em vários nós de armazenamento.


### Banco de Dados NoSQL

Às vezes, os bancos de dados NoSQL são chamados de _bancos de dados não relacionais_ porque suas estruturas são diferentes dos bancos de dados relacionais, como a solução Amazon RDS. Em vez de relacionamentos de linha e coluna, os bancos de dados NoSQL criam uma estrutura para os dados que eles contêm com o uso de pares de _valores-chave_. Com pares de valores-chave, os dados são organizados em itens identificados por chaves exclusivas.

O DynamoDB é um serviço de banco de dados NoSQL totalmente gerenciado que fornece desempenho rápido e previsível para estruturas de dados de documentos e valores-chave. Trata-se de uma opção de banco de dados poderosa e incrivelmente rápida para casos de uso que exigem um esquema flexível, além de ser ideal para aplicações que exigem alto desempenho e scaling contínua.

Um cache em memória é uma camada de armazenamento de alta velocidade que _armazena de forma temporária os dados acessados com frequência na_ memória principal ou _RAM_ de um computador. A recuperação de dados da RAM fornece velocidades de processamento e recuperação extremamente rápidas, em centenas ou milhares de vezes mais rápidas do que os sistemas tradicionais de armazenamento em disco.

Quando as aplicações precisam de informações específicas, primeiro eles verificam o cache antes de solicitá-las da fonte de dados original. Isso reduz a carga nos bancos de dados primários e acelera os tempos de resposta dos usuários finais. Os caches em memória são ideais para armazenar dados de sessão, respostas de API, resultados de consultas de banco de dados e outras informações que as aplicações exigem repetidamente.

O ElastiCache é um serviço de cache em memória totalmente gerenciado e criado para ajudar a reduzir a complexidade da administração de sistemas de cache na memória. Isso significa que é possível continuar usando as mesmas ferramentas e configurações do Redis, Valkey ou Memcached para escalar as workloads. Ele detecta e substitui de forma automática os nós com falha, o que o torna ideal para aplicações que precisam de alto desempenho consistente.

A solução Amazon DocumentDB (compatível com MongoDB) é um serviço totalmente gerenciado projetado para lidar com dados semiestruturados, que são informações em não conformidade com esquemas relacionais rígidos. A solução Amazon DocumentDB é um banco de dados compatível com o MongoDB, portanto, ele gerencia documentos do tipo JSON com esquemas dinâmicos.

A solução AWS Backup simplifica a proteção de dados em vários recursos da AWS e on-premises para fornecer um único painel de monitoração e gerenciamento de backups. Ela elimina a complexidade do gerenciamento de várias estratégias de backup ao oferecer suporte a vários tipos de armazenamento, inclusive volumes da solução Amazon Elastic Block Store (Amazon EBS), sistemas de arquivos da solução Amazon Elastic File System (Amazon EFS) e vários bancos de dados.

O Neptune é um serviço de banco de dados de grafos totalmente gerenciado e desenvolvido para fins específicos. Ele gerencia conjuntos de dados altamente conectados, como os usados em aplicações de redes sociais. Ele se destaca na compreensão de relacionamentos complexos e difíceis de identificar em bancos de dados relacionais tradicionais, como conexões de usuários, redes de amigos e padrões de interação. O Neptune pode manter o alto desempenho mesmo com o aumento da complexidade dos dados e oferece alta disponibilidade com failover e backups automáticos.

A solução Amazon DocumentDB foi projetada para lidar com workloads de bancos de dados, e não para lidar com armazenamento de arquivamento de longo prazo.

O Amazon Aurora é um banco de dados nativo da nuvem que oferece desempenho e disponibilidade superiores aos bancos de dados tradicionais, além de manter a compatibilidade com MySQL e PostgreSQL.