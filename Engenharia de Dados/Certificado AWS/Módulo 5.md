## Redes

Uma Amazon VPC permite provisionar uma seção logicamente isolada da nuvem AWS, em que você pode executar recursos da AWS em uma rede virtual definida por você.

As sub-redes são usadas para organizar seus recursos e podem ser disponibilizadas de forma pública ou privada. Uma sub-rede privada geralmente é usada para conter recursos como um banco de dados que armazena informações transacionais ou de clientes. Uma sub-rede pública geralmente é usada para conter recursos como um site voltado para o cliente.

**Sub-redes** são essencialmente segmentos de sua VPC, o que permite dividir a VPC em seções menores e gerenciáveis. Uma sub-rede é um intervalo de endereços IP na VPC.

**Sub-redes privadas** são projetadas para isolar recursos que não deveriam ser expostos diretamente à internet pública. Nos diagramas, elas são ilustradas com caixas sólidas.

**Sub-redes públicas** são projetadas para fornecer acesso direto à internet aos recursos colocados dentro delas. Para permitir o acesso, elas são conectadas a um gateway da internet. Você aprenderá mais sobre os gateways da internet em uma lição posterior. Nos diagramas, as sub-redes públicas são desenhadas com caixas tracejadas.

As sub-redes são usadas para organizar recursos, compartilhar recursos publicamente ou isolar recursos para mantê-los privados.

Com a solução Amazon VPC, é possível provisionar uma seção isolada da nuvem AWS. Nessa seção isolada, é possível iniciar os recursos na rede virtual que definir. Ela oferece três benefícios principais. Isso ajuda a aumentar a segurança porque é possível proteger e monitorar conexões, rastrear o tráfego e restringir o acesso à instância. A solução Amazon VPC oferece controle total sobre o posicionamento, a conectividade e a segurança de seus recursos. A conveniência de usar a solução Amazon VPC significa que você gastará menos tempo configurando, gerenciando e validando sua rede virtual em comparação com o gerenciamento de rede on-premises.