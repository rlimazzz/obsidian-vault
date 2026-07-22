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

