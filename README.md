# Case de análise de segmentação de clientes
*Dados obtidos pelo case do Ifood, disponível [aqui](https://github.com/ifood/ifood-data-business-analyst-test).*

## Objetivo
Avaliar a base de clientes (pessoal e de compras), encontrar a segmentação e avaliar impacto na interação com as campanhas de marketing.

## Setup
1. Python 3.8.10 on linux (virtual environment)
2. JupyterLab 3.2.8

## Organização
```
case-client-behavior
│   README.md
│   requirements.txt
│
└───data
│     dataset.csv
│     dataset_clean.csv
|     dataset_categorizado.csv
|     storytelling.pdf
|     storytelling.odp
│
└───notebooks
|     limpar_base.ipynb
|     agrupar_clientes.ipynb
|     classificacao.ipynb
|     predicao.ipynb
|     storytelling.ipynb
|
└───models
|     encoder_data_nascimento.pickle
|     encoder_escolaridade.pickle
|     encoder_estado_civil.pickle
|     encoder_renda.pickle
|     model_clientes.pickle
|     classificador.pickle
|     classificador.txt
```

### Algumas observações sobre arquivos
- Todo o processo de análise foi realizado nos arquivos .ipynb dentro do diretório notebooks.
- Os arquivos storytelling no diretório data são documentos que possuem o business como público alvo, apresentando o resultado e direcionamento de toda a análise realizada dentro do diretório notebooks.
- O arquivo model_clientes.pickle é o modelo de cluster para segmentação de clientes.
- O arquivo classificador.pickle é o modelo para predição da probabilidade de um determinado tipo de clientes responder positivamente à campanha de marketing.
- As labels para renda são: "-1000", "1000-5000", "6000-11000", ..., "115000-120000", "+120000".
- As labels para data de nascimento são:"-1940", "1940-1950", "1950-1960", ..., "2000-2010", "+2010".
- O arquivo classificador.txt contêm metadados sobre o modelo salvo, como os campos de entrada, acurácia e porcentagem de falso positivos.
