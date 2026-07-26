## Redes

Uma Amazon VPC permite provisionar uma seção logicamente isolada da nuvem AWS, em que você pode executar recursos da AWS em uma rede virtual definida por você.

As sub-redes são usadas para organizar seus recursos e podem ser disponibilizadas de forma pública ou privada. Uma sub-rede privada geralmente é usada para conter recursos como um banco de dados que armazena informações transacionais ou de clientes. Uma sub-rede pública geralmente é usada para conter recursos como um site voltado para o cliente.

**Sub-redes** são essencialmente segmentos de sua VPC, o que permite dividir a VPC em seções menores e gerenciáveis. Uma sub-rede é um intervalo de endereços IP na VPC.

**Sub-redes privadas** são projetadas para isolar recursos que não deveriam ser expostos diretamente à internet pública. Nos diagramas, elas são ilustradas com caixas sólidas.

**Sub-redes públicas** são projetadas para fornecer acesso direto à internet aos recursos colocados dentro delas. Para permitir o acesso, elas são conectadas a um gateway da internet. Você aprenderá mais sobre os gateways da internet em uma lição posterior. Nos diagramas, as sub-redes públicas são desenhadas com caixas tracejadas.

As sub-redes são usadas para organizar recursos, compartilhar recursos publicamente ou isolar recursos para mantê-los privados.

Com a solução Amazon VPC, é possível provisionar uma seção isolada da nuvem AWS. Nessa seção isolada, é possível iniciar os recursos na rede virtual que definir. Ela oferece três benefícios principais. Isso ajuda a aumentar a segurança porque é possível proteger e monitorar conexões, rastrear o tráfego e restringir o acesso à instância. A solução Amazon VPC oferece controle total sobre o posicionamento, a conectividade e a segurança de seus recursos. A conveniência de usar a solução Amazon VPC significa que você gastará menos tempo configurando, gerenciando e validando sua rede virtual em comparação com o gerenciamento de rede on-premises.

Para permitir que o tráfego público da internet acesse a VPC, é preciso associar um **gateway de internet** à VPC. Um gateway da internet é uma conexão entre uma VPC e a internet. Você pode pensar em um gateway da internet como uma porta que os clientes usam para entrar na cafeteria. Sem um gateway de internet, ninguém pode acessar os recursos na sua VPC.

E se você tiver uma VPC apenas com recursos privados? O exemplo a seguir mostra como funciona um gateway privado virtual. Você pode pensar na internet como o caminho entre sua casa e a cafeteria. É aberto e acessível a qualquer pessoa. É preciso haver uma forma de proteger o tráfego enviado na internet do público, dos provedores de serviços de Internet e de outras pessoas que possam estar tentando rastreá-lo ou interceptá-lo. É aqui que entra uma conexão de rede privada virtual (VPN).

A VPN cria uma conexão mais parecida com um túnel seguro pela internet. Com o uso de criptografia, ele oculta e protege tudo o que você envia e recebe de olhos externos. Um gateway privado virtual é o componente na nuvem AWS que possibilita a conexão desse tráfego protegido em direção à VPC. Com uma conexão VPN, seus dados trafegam de forma privada e segura, escondidos de outras pessoas que usam a mesma rota.

**A solução AWS Client VPN** é um serviço de rede que pode ser usado para conectar os profissionais remotos e redes on-premises na nuvem. Trata-se de um serviço VPN elástico e totalmente gerenciado que aumenta ou diminui a escala verticalmente de forma automática de acordo com a demanda do usuário. Por ser uma solução de VPN na nuvem, e não é preciso instalar e gerenciar hardware nem tentar estimar quantos usuários remotos podem estar conectados ao mesmo tempo.

**A VPN site a site** cria uma conexão segura entre o data center ou as filiais e os recursos da nuvem AWS.

**A solução AWS PrivateLink** é uma tecnologia altamente disponível e dimensionável que pode ser usada para conectar a VPC de forma privada a serviços e recursos, como se eles estivessem na sua VPC. Não é preciso usar um gateway da internet, dispositivo NAT, endereço IP público, conexão Direct Connect ou conexão VPN site a site da AWS para permitir a comunicação com serviços ou recursos da AWS pelas suas sub-redes privadas. Em vez disso, basta controlar os endpoints, sites, serviços e recursos específicos da API que podem ser acessados por meio de sua VPC.

**A solução Direct Connect** é um serviço que permite estabelecer uma conexão privada dedicada entre sua rede e a VPC na nuvem AWS.

A solução Direct Connect forneceria os requisitos de largura de banda para a migração, além das transferências contínuas de dados em sua solução híbrida.

Uma solução Amazon API Gateway é um serviço da AWS voltado para a criação, publicação, manutenção, monitoramento e proteção de APIs em qualquer escala. Ela não seria a escolha certa porque a empresa não está procurando um serviço de API.

Um gateway privado virtual é o componente que permite que o tráfego protegido da internet ingresse na VPC. A solução é perfeita porque restringirá o acesso apenas ao tráfego protegido da internet.

**A movimentação de pacotes de dados que viajam por uma rede**

Quando um cliente solicita dados de uma aplicação hospedada na nuvem AWS, essa solicitação é enviada como um pacote. Um pacote é uma unidade de dados enviada pela internet ou por uma rede.

Ele entra em uma VPC por um gateway da internet. Antes que um pacote possa entrar ou sair de uma sub-rede, ele passará por várias verificações de permissões, sendo uma delas uma ACL de rede associada à sub-rede para a qual o pacote está sendo roteado. As permissões definidas pelas ACLs da rede indicam o que é permitido ou negado. Essas permissões são baseadas em quem enviou o pacote e em como o pacote está tentando se comunicar com os recursos em uma sub-rede.

Uma ACL de rede é um firewall virtual que controla o tráfego de entrada e saída no nível da sub-rede.

Por exemplo, imagine que você está no aeroporto. Os viajantes estão tentando entrar em um país diferente. Você pode pensar nos viajantes como pacotes e no oficial alfandegário como uma ACL de rede. O oficial alfandegário verifica as credenciais dos viajantes quando entram e saem do país. Isso é semelhante à forma como uma ACL de rede verifica as permissões toda vez que um pacote viaja por um limite de sub-rede.

Cada conta AWS tem uma ACL de rede-padrão. Ao configurar a VPC, você pode usar a ACL de rede-padrão da conta ou criar ACLs de rede personalizadas. Em geral, a ACL de rede-padrão da conta permite todo o tráfego de entrada e saída, mas é possível modificá-la ao adicionar suas regras.

**Controle o tráfego de entrada e saída no nível do recurso**

Depois que um pacote entra em uma sub-rede, ele precisa ter as permissões avaliadas para os recursos dentro da sub-rede, como as instâncias da solução Amazon EC2. Um grupo de segurança é o componente da VPC que verifica as permissões de pacotes para uma instância da solução Amazon EC2. Trata-se de um firewall virtual que controla o tráfego de entrada e saída para recursos específicos da AWS, como instâncias da solução Amazon EC2.

Por padrão, um grupo de segurança nega todo o tráfego de entrada e permite todo o tráfego de saída. Para este exemplo, suponhamos que você esteja em um prédio com um porteiro que recebe os visitantes na porta. Podemos pensar nos visitantes como pacotes e no porteiro como um grupo de segurança. Com as configurações padrão, os grupos de segurança não deixam ninguém entrar e permitem que todo o tráfego de saída saia.

![[Pasted image 20260722150102.png]]

**A solução Route 53** é um DNS que fornece uma maneira confiável e econômica de rotear usuários finais para aplicações da internet.

**A solução CloudFront** é um serviço de rede de entrega de conteúdo (CDN) que entrega o conteúdo com tempos de carregamento mais rápidos, economia de custos e confiabilidade.

**A solução Global Accelerator** é um serviço que usa a rede global da AWS para melhorar a disponibilidade, o desempenho e a segurança das aplicações. Ela usa roteamento inteligente de tráfego e failover rápido se algo der errado em um dos locais de seu aplicação.

A conexão da solução AWS Direct Connect forneceria a largura de banda para as grandes cargas de dados e os requisitos de segurança necessários para a conformidade.

A solução Global Accelerator é um serviço de rede projetado para melhorar a disponibilidade e o desempenho de aplicações para usuários globais. Ela faz isso ao fornecer endereços IP estáticos, ao direcionar o tráfego pela rede global da AWS e ao rotear para endpoints ideais de acordo com a integridade, localização do usuário e políticas.

A solução Route 53 é um serviço de sistema de nomes de domínio (DNS) que gerencia o registro do domínio, roteamento de DNS e verificações de integridade. Ela fornece roteamento confiável e eficiente dos usuários para seu site ou aplicações, estejam eles hospedados na AWS ou em outro lugar.

Uma Zona de Disponibilidade é um data center fisicamente isolado ou um conjunto de data centers dentro de uma Região da AWS. Cada AZ tem energia, resfriamento e rede independentes, projetados para melhorar a disponibilidade das aplicações e tolerância a falhas para permitir que os recursos sejam implantados em várias Zonas de Disponibilidade na mesma região.

Um gateway privado virtual é o endpoint de rede privada virtual (VPN) no lado da AWS. Ele fornece uma maneira de estabelecer uma conexão segura e criptografada entre a rede on-premises e a nuvem privada virtual (VPC).

A solução CloudFront acelera a distribuição de seu conteúdo web estático e dinâmico para seus usuários. Ela distribui o conteúdo com segurança e baixa latência por meio de uma rede mundial de data centers chamada de locais da borda.

As ACLs de rede permitiriam o amplo controle de tráfego no nível da sub-rede. As ACLs de rede também têm regras de tipo de permissão e negação.

A solução Direct Connect estabeleceria uma conexão dedicada de uma rede on-premises com uma ou mais nuvens privadas virtuais (VPCs). Ela também pode reduzir os custos de rede, aumentar o throughput da largura de banda e fornecer uma experiência de rede mais consistente que a de conexões baseadas na internet.

A solução Amazon Client VPN é um serviço de rede que pode ser usado para conectar os profissionais remotos e redes on-premises na nuvem. Ela fornece autenticação avançada e acesso remoto e elástico em um serviço totalmente gerenciado.

As ACLs de rede **NÃO** permitiriam segurança em nível de instância. Elas protegeriam somente o nível da sub-rede.

A solução AWS Site-to-Site VPN cria uma conexão segura entre o data center ou as filiais e os recursos da nuvem AWS.

[[Módulo 6]]