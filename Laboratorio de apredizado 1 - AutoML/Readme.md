### Automl-Microsoft-Azure

# Esse é o passo a passo como forma de apredizagem, ultilizando a Azure Machine Learning, realizado como desafio de projeto do Bootcamp Microsoft Azure AI Fundamentals da Dio.

### Primeiro passo 

# Criar uma conta no site https://azure.microsoft.com/pt-br/free
# Sera necessario incerir um cartão de credito para validação dos dados sem cobranças.

### Segundo passo

# Acesse esse link portal.azure.com.
# Navegue ate a area de busca e busque "Azure Machine Learning" na pagina seguinte aperte em criar.

### Terceiro passo

# Dentro da configuração da "Azure Machine Learning" crie um novo "resourse group", "nome" e "região".
# "Resourse group" e "nome" pode renomear do seu do seu gosto, mas a região recomendo "East Us".
# Apertando em "criar", apos aprovação, clique no outro "criar".

### Quarto passo

# Cepois de um tempo de espera, clique em "ir para o recurso".
# Recurso iniciado, agora inicie o estudio, dentro da tela inicial,pode visualizar seu projeto.
# Com ele aberto voce busca a opção, "Automated ML" clica e la dentro clica em "new ML automated job"

### quinto passo

# Agora no preenchimento, só altera os campo "Job name" colocando "mslearn-bike-automl", "New experiment name" colocando "mslearn-bike-rental", "description" colocando "Aprendizado de máquina automatizado para a previsão de aluguel de bicicleta".
# Na proxima aba "task Type" vamos modificar, "Select task type" para "Regression" e clica em "Create".
 
### Sexto passo

# Nessa aba que abriu, coloca o nome, o mesmo que o anterior, a descrição e "type" como "tabular".
# Depois dessa aba aparrecerá o "data source" nele voce seleciona "From web file",e na proxima aba coloca o link "https://aka.ms/bike-rentals".
# Nas proximas abas até a aba "Review" é apenas next e create.

### Setimo passo 

# Depois de criar seleciona seu projeto e parte em next.
# Nessas primeira aba "task settings", altera-se as opçoes, "Target column" para "rentals(integrecion)", clica em "view "addicitional configuraion settings" nessas aba paralela desmarca as opções e em "Allowed models" marca "RandomForest" e "LightGBM" e salva.
# Voltando para a aba anterior, clica em Limits e nessa aba paralela nas proximas 3 opções deixa com o valor 3, na "Metroc score threshold" valor 0.085 nas outras duas digita 15 e marca a caixinha.
# Em "Validation type" colca em "train-validation-slit" clicando em next nos proximos e criar seu trabalho.

### Oitavo passo 

# Quando termina a validação voce clica em "Task" na aba lateral e clica no seu projeto.
# Dentre as opções superiores destaca-se as "Metrics" que retorna todos os dados estatiscos do projeto.
# Além disso na primeira opção "Overview" dentro dela tem a "Deploy" que tem a opção "Web Service" detro dela voce cria um modelo deploy com as informações anteriores.
# Quando ela finalizar vai na opção "Test" e coloca o json:

 {
   "Inputs": { 
     "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }

 # Resultando em um numero previsto de quantidades de bikes para alugar.




