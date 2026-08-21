## Arquitetura de Dados

Serve para determinar o ciclo de vida de como usamos os dados.

ETL ==(Extract, Transform, Load)== - Filter -> Extract -> Cleanse -> Encode/Decode, Aggregate/Split, Join, Convert -> Staging -> Load -> Data Tables.

Commit log - É o histórico lógico de todas alterações salvas (commits) em um sistema de controle de versão ou banco de dados.

ELT ==(Extract, Load, Transform)== - Extract -> Load -> Staging Tables -> Data Tables.

Data Lake - Podemos jogar qualquer tipo de dado. Algumas características são:
	Repositório centralizado : projetado para armazenar, processar e proteger grandes quantidades de dados. Pode armazenar todos tipos de dados.

O **batch data** (dados em lote) refere-se a ==grandes volumes de informações reunidas, armazenadas e processadas de uma só vez em períodos programados, em vez de tratadas de forma contínua ou em tempo real==.

Arquitetura Medallion : ==é um padrão de design de dados usado para organizar e refinar informações em um _data lakehouse_ de forma progressiva==.
	Bronze : Dados brutos, usados para salvar caso aconteça alguma coisa em alguma etapa à frente.
	Silver : Filtrar, limpar e complementar os dados ingeridos na camada bronze, é uma camada intermediária para meio que transformar os dados.
	Gold : Tabelas selecionadas em nível de negócio, organizadas em banco de dados específicos para cada negócio.

