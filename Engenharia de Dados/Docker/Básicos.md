O docker é um conjunto de plataforma de serviços que usam virtualização de nível de sistema operacional para entregar pacotes chamados contêineres. Tais contêineres, são isolados uns dos outros e cada contêiner agrupa seu próprios softwares, bibliotecas e arquivos de configuração, onde eles podem comunicar uns com os outros por meios de canais bem definidos de comunicação. Todos os contêineres são executados por um único kernel do sistema operacional, portanto usam menos recursos do que as máquinas virtuais. Com o Docker podemos ver quais foram as ações feitas no nosso contêiner, no caso recebemos ações do tipo GET do usuário que está acessando o site.

_Fine-Grained Access Control(FGAC)_ : É um método de segurança que trabalha apenas com o necessário, sendo assim o usuário apenas tem acesso às informações estritamente necessárias para realizar suas tarefas. É um modelo frequentemente associado ao _Attribute-Based Access Control_(ABAC) que considera atributos para tomadas de decisão, por exemplo: 

- **Atributos do Usuário:** Cargo, departamento, nível de senioridade, certificações de treinamento, etc.

- **Atributos do Recurso:** Sensibilidade do dado, tipo de arquivo, proprietário do dado, localização do arquivo, etc.
    
- **Atributos do Ambiente:** Localização geográfica do usuário, horário do acesso, tipo de dispositivo utilizado (corporativo ou pessoal), nível de segurança da rede, etc.
    
- **Atributos da Ação:** A operação que o usuário está tentando realizar (ler, escrever, editar, excluir, aprovar, etc.).

Por exemplo, uma política de FGAC poderia estipular que um "Gerente de Vendas" (atributo do usuário) pode "visualizar" (atributo da ação) os "dados de vendas do seu próprio time" (atributo do recurso) apenas durante o "horário comercial" (atributo do ambiente) e a partir de um "dispositivo corporativo" (atributo do ambiente).