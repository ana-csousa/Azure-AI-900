# DIO | Azure-AI-900 | Desafio de Projeto

### 👩‍💻Trabalhando com Machine Learning na Prática no Azure ML

       Proposta: Criar um modelo de previsão relacionado a aluguel de bicicletas.


 📚Elaboração:

 1- Criar uma conta free no portal da Azure;

 2- Logar no portal e criar um novo recurso;

 3- Pesquisar por Azure Machine Learning e clicar em criar;

 4- Será exibida a workspace de criação, aplicar as configurações abaixo:

    1- Na Aba "Basic" atribuir ou criar(se já não tiver criado):
        [uma Subscription] 
        [um Resource group]
        [Name da workspace]
        [Escolher a Region]

    ... Avançar/Next para proxima Aba 


    2- Na Aba "Networking" selecionar:
        [Public] 

    ...Finalizar clicando em Review + Create

    (Aguardando a finalização  do Deployment)

5- Criação do ML automatizado. 

    1- Dentro da workspace criada, escolher a opção "ML Automatizado";

        Definindo:
        nome do trabalho: mslearn-bike-automl
        nome do experimento: mslearn-bike-retal
        Inserindo a descrição
        ...Avançar

        Tipo de tarefa e de dados...
        Tipo de tarefa: Regressão
        Clicar em Criar um ativo de dados
        Nome do ativo de dados: Aluguel de bicicletas
        Inserindo a descrição
        Tipo de ativo de dados: Tabela (mltable)
        Fonte para arquivo de dados: De arquivo locais (tive que baixar e descompactar).

        Apos esses passos, clicar em criar e aguardar a geração dos dados. 

        Configurando a tarefa...
        Coluna de destino: rentals(integer)

        Em configurações adicionais...
        Métrica primária : NormalizedRootMeanSquaredError
        Desmarcar:
        * Explique o melhor modelo 
        * Habilitar empilhamento de conjunto 
        * Usar todos os modelos suportados
        
        Modelos permitidos : Selecione apenas RandomForest e LightGBM 

        Limites...
        Máximo de ensaios :3
        Máximo de ensaios simultâneos :3
        Máximo de nós :3
        Limite de pontuação métrica : 0.085
        Tempo limite do experimento :15
        Tempo limite de iteração :15
        Marcar a opção: Habilitar rescisão antecipada

        Em Validação e teste ...
        Tipo de validação : Divisão de validação de trem
        Porcentagem de dados de validação : 10
        Conjunto de dados de teste : Nenhum
        Calcular :

        tipo de computação : Sem servidor
        Tipo de máquina virtual : CPU
        Camada de máquina virtual : Dedicada
        Tamanho da máquina virtual : Standard_DS3_V2*
        Número de instâncias : 1

        ...Avançar

6- Aguardar a conclusão (em torno de 15 min) para ter acesso as metricas. 

💻 [link do exercicio base](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)


