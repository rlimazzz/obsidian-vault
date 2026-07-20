## Amazon EC2

Amazon Elastic Compute Cloud é um serviço que permite alugar máquinas virtuais(servidores) na nuvem. Ele elimina a necessidade de comprar hardware físico, permitindo criar, configurar e escalar sistemas rapidamente de acordo com a demanda do seu negócio, pagando apenas pelo tempo de uso.

A multilocação possibilita que diversas máquinas virtuais, embora isoladas entre si, compartilhem os recursos de um mesmo host físico.

A multilocação possibilita que diversas máquinas virtuais, embora isoladas entre si, compartilhem os recursos de um mesmo host físico.

Você precisa escolher o tipo de instância EC2 (a potência desejada) e a Imagem de máquina da Amazon (AMI), que determina o sistema operacional e o software da sua instância.

*Tipos de Instância*
	Uso Geral
	Otimizadas para computação
	Otimizadas para memória

API : Interface de programação de aplicações

A AWS CLI foi projetada para tarefas repetitivas e automação, e não para provisionamento manual único, o que é mais adequado para o console.

O cliente é responsável por configurar, proteger e gerenciar o sistema operacional, a rede e as aplicações em suas instâncias do EC2.

AMI significa Amazon Machine Image(Imagem de Máquina da Amazon). Em termos simples, é um modelo ou uma "fotografia" exata que contém o sistema operacional(como Linux ou Windows), aplicativos e configurações necessários para criar um servidor virtual no Amazon EC2.

Os Savings Plans oferecem descontos para uso consistente, mas não oferecem economias tão significativas quanto as instâncias spot.

O Amazon EC2 Auto Scaling ajusta automaticamente o número de instâncias do EC2 com base nas mudanças na demanda da aplicação, oferecendo melhor disponibilidade.

O serviço Elastic Load Balancing (ELB) opera distribuindo de forma automática o fluxo de tráfego de uma aplicação entre diversos recursos, como as instâncias EC2, com o objetivo de otimizar o desempenho e a confiabilidade. O balanceador de carga atua como um ponto centralizado de entrada para todo o tráfego web destinado a um grupo de Auto Scaling. À medida que a quantidade de instâncias EC2 varia em resposta à demanda, todas as requisições são inicialmente recebidas pelo balanceador de carga. A partir daí, o tráfego é distribuído uniformemente pelas instâncias disponíveis.

![[Pasted image 20260720075511.png]]

O ELB e o Auto Scaling trabalham juntos para gerenciar o nível de demanda com eficiência. O ELB é responsável por distribuir uniformemente o tráfego de entrada em várias instâncias do EC2. Isso garante que nenhuma instância fique sobrecarregada. Ele também serve como um único ponto de entrada para o tráfego em um grupo de Auto Scaling, direcionando as solicitações para os recursos apropriados.

Enquanto isso, o Auto Scaling ajusta automaticamente o número de instâncias do EC2 com base na demanda. Ele adiciona ou remove instâncias conforme necessário para otimizar o desempenho e o uso de recursos. Juntos, o ELB e o Auto Scaling ajudam a manter a confiabilidade da aplicação e a eficiência de custos.

![[Pasted image 20260720080658.png]]
![[Pasted image 20260720080717.png]]

Em sistemas fortemente acoplados, os componentes são altamente interdependentes. Se um componente falhar, isso pode causar falhas em cascata. Em contraste, os sistemas fracamente acoplados têm componentes que operam de forma independente, portanto, a falha de um componente não interrompe todo o sistema.

Essa é a melhor abordagem. Os Savings Plans são ideais para workloads críticas que precisam de capacidade consistente e preços previsíveis. As instâncias spot oferecem economias significativas para trabalhos que não são urgentes e podem tolerar interrupções.