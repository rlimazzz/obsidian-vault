Um sistema distribuído é um conjunto de computadores independentes, que para o usuário parece um único sistema. Os computadores se comunicam por troca de mensagens e não há memória compartilhada nem relógio global.

Características:
- Compartilhamento de recursos : vários usuários usam dados, serviços e hardware em comum.
- Concorrência : muitas coisas acontecem ao mesmo tempo.
- Sem tempo global : cada máquina tem seu próprio relógio.
- Falhas independentes : uma máquina pode cair enquanto as outras continuam.
- Coordenação explícita : as máquinas precisam combinar as coisas por mensagens.
- Heterogeneidade: Hardware, sistemas operacionais e redes diferentes.

Descentralizado x Distribuído

Descentralizado: espalhado em várias máquinas por necessidade(funcional ou organizacional). Exemplo: blockchain, em que ninguém confia num dono único.

Distribuído: espalhado em várias máquinas por desempenho e escalabilidade.

Logicamente centralizado, fisicamente distribuído: o cliente vê um ponto único(por exemplo, um API gateway), mas por trás há vários serviços e instâncias.

Objetivos de projeto:
- Compartilhamento de recursos: facilitar o acesso a recursos remotos, escondendo onde eles estão.
- Transparência : esconder do usuário que o sistema é distribuído.
- Abertura : usar interfaces padrão, o que garante interoperabilidade, composição, portabilidade e extensibilidade.
- Confiabilidade: disponibilidade, confiabilidade, segurança contra dados(safety) e manutenibilidade.
- Segurança(security): confidencialidade, integridade, autenticação, autorização e não repúdio.
- Escalabilidade: crescer sem perder desempenho.

### Técnicas de escalabilidade

Descentralização : evita gargalos.
Particionamento: funções diferentes em máquinas diferentes.
Replicação: cópias da mesma função, o que melhora desempenho, proximidade e tolerância a falhas.
Cache: guardar perto o que é mais acessado.

### Middleware

MIddleware é uma camada entre o sistema operacional e as aplicações, e é a peça-chave para atingir os objetivos acima.
	Oferece a mesma interface em todo lugar, o que aumenta a transparência e a abertura.
	Concentra num só lugar a tolerância a falhas, a segurança e a escalabilidade.

### Tipos de sistemas distribuídos

Computação distribuída : processamento pesado com cluster, grid, nuvem, HPC.

Sistemas de informação distribuídos : Dados e transações com processamento de transações, integração de sistemas empresariais, BDs distribuídos, middleware de mensagens.

Sistemas pervasivos: Integrados ao ambiente com IoT, computação móvel, redes de sensores, edge computing e computing continuum.

### Armadilhas sobre sistemas distribuídos

É errado assumir que: 
- A rede é confiável
- A rede é segura
- A rede é homogênea
- A topologia não muda
- A latência é zero
- A largura de banda é infinita
- O custo de transporte é zero
- Existe um único administrador

Todas são falsas.

### Trade-offs

**Consistência x Disponibilidade**: dados sempre iguais em todas as cópias, ou sistema sempre respondendo?
**Latência x Vazão(throughput)**: responder rápido cada pedido, ou processar muitos pedidos no total?
**Centralização x Descentralização**: simplicidade e controle, ou escala e resiliência?

### Resumo rápido do capítulo 1

Um sistema distribuído são **várias máquinas que parecem uma só**. Elas se comunicam **por mensagens**, sem memória nem relógio compartilhados. Os objetivos de projeto são **compartilhar recursos, ser transparente, aberto, confiável, seguro e escalável** e o middleware é a camada que viabiliza isso. Há três tipos (**computação, informação e pervasivos**).