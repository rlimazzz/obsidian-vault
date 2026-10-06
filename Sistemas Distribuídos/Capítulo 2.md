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


