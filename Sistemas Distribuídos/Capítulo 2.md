### Tipos de arquitetura
#### 1.1. Arquitetura em camadas

Cada camada usa os serviços da camada de baixo e oferece serviços à de cima. Há três variações:

- **(a) pura:** só chama a camada imediatamente abaixo;
- **(b) mista:** pode pular camadas;
- **(c) com _upcalls_:** a camada de baixo chama a de cima (_callback_).
#### 1.2 Arquitetura baseada em objetos e em serviços

- Os componentes são **objetos** que se comunicam por **chamadas de procedimento**, e essas chamadas podem ser **remotas**, pela rede.
- **Encapsulamento:** o objeto esconde seus dados e oferece métodos, sem revelar a implementação.
- Essa é a base das **arquiteturas orientadas a serviços (SOA)**.

#### 1.3 Arquitetura RESTful ⭐

O sistema é visto como uma **coleção de recursos**, e cada recurso é gerenciado por um componente. As operações sobre os recursos formam o **CRUD** (criar, ler, atualizar, apagar).

Os quatro princípios do REST:

1. Os recursos são identificados por **um único esquema de nomes** (URIs).
2. **Todos os serviços oferecem a mesma interface.**
3. As mensagens são **autodescritivas**.
4. **Sem estado (_stateless_):** depois de executar uma operação, o servidor **esquece** o cliente.

#### 1.3 Arquitetura RESTful ⭐

O sistema é visto como uma **coleção de recursos**, e cada recurso é gerenciado por um componente. As operações sobre os recursos formam o **CRUD** (criar, ler, atualizar, apagar).

Os quatro princípios do REST:

1. Os recursos são identificados por **um único esquema de nomes** (URIs).
2. **Todos os serviços oferecem a mesma interface.**
3. As mensagens são **autodescritivas**.
4. **Sem estado (_stateless_):** depois de executar uma operação, o servidor **esquece** o cliente.

**REST × SOAP:** a pergunta "o que se pode concluir?" dos slides costuma cair.

- **SOAP:** `bucket.create("mybucket")`. Cada serviço tem **operações próprias**, então a interface é rica, mas complexa e específica.
- **REST:** `PUT https://mybucket.s3.amazonaws.com/`. A **interface é simples e igual para todos**, mas a complexidade vai para os **parâmetros** (URI, cabeçalhos, corpo da mensagem).
- 👉 **Conclusão:** nenhum dos dois é melhor em tudo. A complexidade não desaparece, **só muda de lugar**: no SOAP ela fica na interface, no REST fica nos parâmetros.
- 
### 2. Middleware

O middleware funciona como **o "sistema operacional" dos sistemas distribuídos**: reúne componentes e funções comuns, para que cada aplicação não precise implementá-los de novo.


### 3. Arquiteturas de sistema

#### 3.1 Centralizadas: cliente-servidor

- **Servidores** oferecem serviços e **clientes** usam esses serviços.
- Eles podem estar em máquinas diferentes.
- A comunicação segue o modelo **requisição/resposta**.

**Organizações multicamadas físicas:**

- **1 camada:** terminal burro + mainframe.
- **2 camadas:** cliente + servidor único. As configurações de (a) a (e) dos slides mostram o quanto fica no cliente, indo do **cliente magro** (só a interface fica no cliente) ao **cliente gordo** (interface, lógica e parte dos dados ficam no cliente).
- **3 camadas:** cada camada lógica em uma máquina. Nesse caso o **servidor de aplicação é cliente e servidor ao mesmo tempo**: atende o cliente e faz pedidos ao servidor de banco de dados.

**Exemplo: NFS (Network File System).** Cada servidor oferece uma **visão padronizada** do seu sistema de arquivos local, seja qual for a implementação por baixo. Há dois modelos de acesso:

- **Acesso remoto** (NFS): o arquivo **fica no servidor** e o cliente executa operações nele remotamente.
- **Upload/download** (FTP, Dropbox): o cliente **baixa** o arquivo, trabalha **localmente** e depois **envia de volta**.

**Exemplo: a Web.**

- **No início:** o site era um conjunto de arquivos HTML ligados por hiperlinks. O servidor só buscava arquivos, e o navegador exibia.
- **Depois:** o site passou a ser construído em torno de um **banco de dados**, e um programa separado (**CGI**) montava a página dinamicamente.

#### 3.2 Distribuição vertical × horizontal ⭐

- **Vertical:** cada **camada lógica** (interface, processamento, dados) roda em uma **máquina diferente**.
- **Horizontal:** um cliente ou servidor é **dividido em partes equivalentes**, e cada parte cuida de **uma fatia dos dados**. Exemplos: sharding, clusters web.

#### 3.3 Peer-to-peer (P2P)

**Todos os processos são iguais**: cada um é cliente e servidor ao mesmo tempo, papel chamado de **servente** (_servent_). Os nós formam uma **rede de sobreposição (_overlay_)**, que é uma rede lógica construída por cima da rede física.

##### P2P estruturado

Usa um **índice sem semântica**: `chave = hash(dado)`, e o sistema armazena pares **(chave, valor)**. Isso é uma **DHT** (tabela hash distribuída).

- **Hipercubo:** buscar o dado de chave _k_ equivale a rotear a consulta até o nó cujo identificador é _k_.
- **Chord** ⭐:
    - Os nós ficam organizados num **anel**, cada um com um identificador de _m_ bits.
    - O dado de chave _k_ fica no **sucessor** de _k_, ou seja, o **primeiro nó com id ≥ k**.
    - **Atalhos** (_finger table_) aceleram a busca, levando a **O(log N)** saltos.
    - Exemplo dos slides: `lookup(3)` a partir do nó 9 percorre 28 → 1 → 4.

##### P2P não estruturado

Cada nó tem uma lista **aleatória** de vizinhos, então a rede se parece com um **grafo aleatório**. Há duas formas de busca:

- **Inundação (_flooding_):** o nó repassa a busca para **todos os vizinhos**, e quem já viu a busca a ignora. Ela é limitada por um **TTL** (número máximo de saltos).
- **Caminhada aleatória (_random walk_):** o nó repassa a busca para **um vizinho aleatório**, que faz o mesmo, e assim por diante.

**Comparação entre as duas** (contas dos slides):

- **Caminhada aleatória:** o número esperado de nós consultados é **S ≈ N/r**, em que _r_ é o número de réplicas do dado. Com r/N = 0,001, **S ≈ 1000**.
- **Inundação:** depois de _k_ passos com _d_ vizinhos, foram atingidos R(k) = d(d−1)^(k−1) nós. Com d = 10 e k = 4, são **7290** nós consultados.
- 👉 A **caminhada aleatória gasta menos mensagens**, mas **pode demorar mais**. A **inundação é mais rápida**, mas **sobrecarrega a rede**.

##### Super-peers

Quebram a simetria de propósito: alguns nós mais fortes funcionam como **índices** ou **brokers**, o que melhora as buscas e a decisão de onde guardar os dados.

##### BitTorrent

1. O usuário busca o arquivo num diretório global e recebe um arquivo **.torrent**.
2. O .torrent aponta para um **tracker**, servidor que sabe quais nós têm pedaços do arquivo.
3. O nó entra no **enxame (_swarm_)**, recebe um pedaço de graça e depois **troca pedaços** com outros nós.

É um exemplo de **arquitetura híbrida**: o tracker é centralizado e a troca de pedaços é P2P.