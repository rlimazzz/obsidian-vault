Correto. O sobreajuste ocorre quando um modelo aprende com os dados de treinamento e não consegue ter um bom desempenho quando recebe novos dados. Esse fator explica por que o modelo tem alta acurácia nos dados de treinamento e baixa acurácia nos dados de teste.

Incorreto. Um tempo de treinamento insuficiente levaria a uma baixa acurácia nos dados de treinamento e nos dados de teste. Porém, isso não explica por que o modelo teria alta acurácia nos dados de treinamento.

Incorreto. O subajuste ocorre quando um modelo não identifica as relações nos dados de treinamento. Isso levaria a uma baixa acurácia nos dados de treinamento e nos dados de teste.

Incorreto. O excesso de dados de treinamento não limita a acurácia de um modelo por si só. Esse fator não explica por que um modelo tem alta acurácia nos dados de treinamento e baixa acurácia nos dados de teste.

Correto. O Amazon Textract é um serviço totalmente gerenciado que pode detectar e extrair texto e dados de imagens, arquivos PDF e documentos digitalizados. Um dos casos de uso do Amazon Textract é o processamento de faturas e recibos. Por exemplo, ele pode detectar endereços de cobrança e de envio automaticamente com base em imagens.

## Amazon SageMaker

Incorreto. O Monitor de Modelos do SageMaker monitora a qualidade dos modelos e dados de ML na produção. Não é possível usar o Monitor de Modelos do SageMaker para criar um registro de informações essenciais do modelo, como classificações de risco, detalhes de treinamento e resultados de avaliação.

Incorreto. Você pode usar o Gerenciador de Perfis do SageMaker para definir permissões de usuário para atividades de ML. Não é possível usar o Gerenciador de Perfis do SageMaker para criar um registro das informações essenciais do modelo.

Correto. Você pode usar os cartões de modelo do SageMaker para criar registros e documentar detalhes sobre modelos de ML em um único local. Os cartões de modelo do SageMaker permitem o desenvolvimento de modelos transparentes e explicáveis, fornecendo documentação abrangente e imutável das informações essenciais do modelo.

Incorreto. O SageMaker Model Dashboard é um local central para visualizar, pesquisar e explorar todos os modelos em uma conta da AWS. O SageMaker Model Dashboard fornece informações sobre implantação, uso, monitoramento de desempenho e monitoramento de modelos. Não é possível usar o SageMaker Model Dashboard para criar um registro de informações essenciais do modelo, como classificações de risco, detalhes de treinamento e resultados de avaliação.

Correto. ROUGE é uma métrica que pode ser usada para avaliar a qualidade de resumo e geração de texto. É possível usar essa métrica para avaliar o desempenho de um FM de geração de texto.

Incorreto. É possível usar a pontuação F1 para avaliar a acurácia de um modelo com relação à classificação binária. As pontuações F1 usam precisão e recall para avaliar a exatidão com que um modelo classifica corretamente a classe certa. Não é possível usar a pontuação F1 para avaliar o desempenho de um FM de geração de texto.

Correto. RAG é o processo de melhorar a qualidade e a consistência dos LLMs consultando uma base de conhecimento externa que está fora das fontes de dados de treinamento do LLM. A RAG consulta a base de conhecimento externa antes de gerar uma resposta. Você pode usar a RAG para fornecer ao modelo acesso a fontes de conhecimento externas com o mínimo esforço de desenvolvimento.

Incorreto. O ajuste fino é o processo para treinar e refinar ainda mais um LLM pré-treinado em um conjunto de dados menor e direcionado. O objetivo de ajustar um LLM pré-treinado é manter a capacidade original do modelo e adaptá-lo a casos de uso mais especializados. O ajuste fino exige um esforço de desenvolvimento adicional para treinar o modelo.

Correto. O Amazon Bedrock é um serviço totalmente gerenciado que fornece uma API unificada para acessar modelos de base (FMs) conhecidos. O Amazon Bedrock comporta modelos de geração de imagens de provedores, como a Stability AI ou a AWS. Você pode usar o Amazon Bedrock para consumir FMs por meio de uma API unificada sem a necessidade de treinar, hospedar ou gerenciar modelos de ML. Essa é a solução mais adequada para uma empresa que não deseja treinar ou gerenciar modelos de ML para geração de imagens.


## ML

Correto. A engenharia de atributos é um método para selecionar e transformar variáveis ao criar um modelo preditivo. A engenharia de atributos inclui a criação, transformação, extração e seleção de atributos. A engenharia de atributos aprimora os dados aumentando o número de variáveis no conjunto de dados de treinamento até, finalmente, melhorar o desempenho do modelo.

Incorreto. O monitoramento de modelos é um componente do ciclo de vida de ML que captura dados e os compara com os dados de treinamento. Você pode usar o monitoramento de modelos para identificar problemas de qualidade de dados, problemas de qualidade do modelo, desvio de viés e desvio de atribuição de recursos. O monitoramento de modelos não aumenta o número de variáveis no conjunto de dados de treinamento nem modifica o comportamento do algoritmo.

Incorreto. A avaliação do modelo é uma etapa do pipeline de desenvolvimento de ML que ocorre após o treinamento do modelo. Você pode usar a avaliação do modelo para determinar o desempenho e as métricas de um modelo. A avaliação do modelo não aumenta o número de variáveis no conjunto de dados de treinamento nem modifica o comportamento do algoritmo.

Correto. A coleta de dados é uma etapa para rotular, ingerir e agregar dados usada para treinamento de modelos de ML. Durante a coleta de dados, dados de várias origens são ingeridos e agregados. Em seguida, eles são rotulados. O estágio de coleta de dados envolve a coleta de dados brutos adicionais, o que pode aumentar o número de variáveis no conjunto de dados de treinamento.

Incorreto. O ajuste de hiperparâmetros é um método para ajustar o comportamento de um algoritmo de ML. Você pode fazer alterações em um modelo de ML usando o ajuste de hiperparâmetros para modificar o comportamento do algoritmo. No entanto, o ajuste de hiperparâmetros não aumenta o número de variáveis no conjunto de dados de treinamento.