## Armazenamento

### Armazenamento em bloco

O armazenamento em bloco fornece volumes de armazenamento persistentes e de baixa latência em nível de bloco que se conectam a instâncias do EC2, como discos rígidos físicos. Os volumes de armazenamento em bloco podem ser criptografados, copiados por meio de snapshots e modificados durante o uso sem interromper a instância. A AWS oferece dois serviços principais de armazenamento em blocos:

- _Armazenamento de instância do Amazon EC2_  
    Um armazenamento em blocos não gerenciado, persistente e de alto desempenho diretamente conectado às instâncias do EC2 para dados temporários.
    
- _Amazon Elastic Block Store (EBS)_  
    Um serviço gerenciado que fornece volumes persistentes de armazenamento em blocos para instâncias do EC2, oferecendo vários tipos para diferentes workloads

### Armazenamento de objetos

O armazenamento de objetos é uma arquitetura de armazenamento de dados que gerencia dados como objetos em um espaço de endereço plano. Ele oferece escalabilidade ilimitada para que você possa armazenar grandes quantidades de dados não estruturados sem se preocupar com restrições de capacidade. O armazenamento de objetos fornece recursos aprimorados de metadados para fornecer gerenciamento, pesquisa e análise de dados mais eficientes em grandes conjuntos de dados.

O seguinte é o principal serviço de armazenamento de objetos da AWS:

- _Amazon Simple Storage Service (S3)_  
    Um serviço de armazenamento de objetos dimensionável e totalmente gerenciado para armazenar e recuperar qualquer quantidade de dados de qualquer lugar.

### Armazenamento de arquivos

Os serviços de armazenamento de arquivos da AWS fornecem sistemas de arquivos compartilhados acessíveis por meio de redes, para que vários usuários e aplicações possam acessar os mesmos dados simultaneamente. Eles oferecem escalabilidade e flexibilidade para que você possa expandir a capacidade de armazenamento à medida que as necessidades aumentam sem gerenciar a infraestrutura física. A AWS oferece dois serviços principais de armazenamento de arquivos:

- _Amazon Elastic File System (EFS)_  
    Um sistema de arquivos NFS totalmente gerenciado e dimensionável para uso com AWS Cloud Services e recursos on-premises.
    
- _Amazon FSx_  
    Um serviço de armazenamento de arquivos totalmente gerenciado para sistemas de arquivos populares, como Windows, Lustre e NetApp ONTAP.

O armazenamento de instância do Amazon EC2 não é um serviço autônomo de armazenamento em blocos da AWS. Em vez disso, ele se refere ao armazenamento em nível de bloco que está fisicamente conectado ao computador host da instância EC2. Dependendo do tipo de instância, o armazenamento de instâncias do EC2 pode ser anexado como armazenamento padrão. Como seus dados são perdidos quando uma instância é interrompida ou encerrada, o armazenamento de instâncias do EC2 é melhor para necessidades temporárias de armazenamento baseado em memória, como buffers, caches e dados temporários. Não é recomendado para aplicações que exigem retenção de dados.

O Amazon EBS disponibiliza volumes de _armazenamento no nível de bloco persistentes_ para uso com instâncias do Amazon EC2. Os volumes do EBS funcionam como discos rígidos externos, oferecendo desempenho consistente e de baixa latência para workloads como bancos de dados e sistemas de arquivos.

Os snapshots do EBS são backups pontuais do volume do EBS. Eles podem ser usados para recuperação de desastres, migração de dados, redimensionamento de volumes e para criar backups consistentes das workloads de produção. Os snapshots do EBS são incrementais, então eles só salvam os blocos no volume que foram alterados após o snapshot mais recente.

Você pode automatizar a criação, retenção e exclusão de snapshots do EBS usando o Amazon Data Lifecycle Manager. O Amazon Data Lifecycle Manager pode programar snapshots fora do horário de pico para minimizar o impacto no desempenho e excluir automaticamente backups desatualizados para controlar os custos de armazenamento. É particularmente valioso para implantações em grande escala, nas quais o gerenciamento manual de snapshot seria demorado e propenso a erros.

Amazon S3 é um serviço de armazenamento de objetos totalmente gerenciado e altamente disponível para armazenar e recuperar qualquer quantidade de dados como objetos. Ele oferece durabilidade de 99,999999999%, o que significa que seus dados estão altamente protegidos contra perdas e oferece atributos como versionamento, gerenciamento do ciclo de vida e várias classes de armazenamento para otimizar custos.

O Amazon S3 armazena arquivos como objetos em contêineres conhecidos como buckets, e cada objeto pode variar em tamanho de alguns bytes a vários terabytes. Ele se integra perfeitamente a outros serviços da AWS e oferece suporte a uma ampla variedade de casos de uso, desde backups básicos até data lakes complexos.

Ao criar um bucket, você especifica seu nome e a região em que ele residirá. Os buckets podem ser configurados com várias configurações, incluindo versionamento, registro e permissões de acesso.

As configurações do S3 Block Public Access substituem as políticas de bucket, impedindo o acesso público mesmo quando as políticas o permitem.

Os buckets do S3 podem ser acessados globalmente, independentemente da região em que foram criados, desde que tenham as permissões adequadas.

O S3 Standard é considerado armazenamento de uso geral para aplicações em nuvem, sites dinâmicos, distribuição de conteúdo, aplicativos móveis e de jogos e análise de big data. Quando você faz upload um objeto no Amazon S3 sem especificar uma classe de armazenamento, o objeto é adicionado ao S3 Standard por padrão.

O Amazon EFS foi projetado para acesso compartilhado simultâneo de várias instâncias do EC2 em diferentes Zonas de Disponibilidade com desempenho consistente. Isso possibilita que equipes globais colaborem nos mesmos arquivos.