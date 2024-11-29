# Análise de Preços de Ações usando SARIMAX

## 📋 Descrição
Este projeto tem como objetivo analisar e prever os preços de ações usando o modelo SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous regressors). O script `sarimax_var_exogenas.py` carrega dados de um arquivo CSV chamado `price.csv`, realiza análises exploratórias e treina um modelo SARIMAX para fazer previsões de preços futuros.

## 🎯 Objetivo do Projeto
- Analisar padrões e tendências nos preços das ações
- Criar um modelo preditivo para prever preços futuros de ações
- Avaliar o desempenho do modelo SARIMAX na previsão de preços

## 📊 Dados
- Fonte dos dados: Arquivo CSV `price.csv`
- Período de coleta: 2008-10-01 a 2019-09-27
- Quantidade de registros: 2769
- Principais variáveis: 'Date', 'Open', 'High', 'Low', 'Close', 'Adj Close', 'Volume'

## 🔍 Metodologia
### 1. Preparação dos Dados
- Carregamento dos dados do arquivo CSV
- Criação da coluna 'Mean' calculando a média entre 'Low' e 'High'
- Criação da coluna 'Actual' deslocando a coluna 'Mean' para servir como variável alvo
- Conversão da coluna 'Date' para datetime e definição como índice

### 2. Análise Exploratória
- Plotagem dos preços de fechamento ao longo do tempo
- Plotagem do volume de negociação ao longo do tempo
- Decomposição sazonal dos preços médios
- Normalização das variáveis usando MinMaxScaler

### 3. Modelagem
- Divisão dos dados em conjuntos de treinamento e teste
- Treinamento do modelo SARIMAX usando auto_arima para encontrar os melhores parâmetros
- Previsão dos preços usando o modelo treinado
- Plotagem dos preços reais vs previstos
- Cálculo do erro médio quadrático (MSE) para avaliar o desempenho do modelo

## 📈 Resultados
- O modelo SARIMAX foi capaz de capturar as tendências gerais dos preços das ações
- As previsões seguiram de perto os preços reais, indicando um bom desempenho do modelo
- O erro médio quadrático (MSE) obtido foi de 0.00013821411633853532, indicando um erro relativamente baixo

## 🛠️ Tecnologias Utilizadas
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn
- Pmdarima

## 📂 Estrutura do Projeto
```
projeto/
│   
├── data/
│   └── price.csv            # Dados de preços das ações
│
├── sarimax_var_exogenas.py  # Script principal de análise e modelagem
│
├── requirements.txt         # Dependências do projeto 
└── README.md
```

## 🚀 Como Executar o Projeto
```bash
# Clone este repositório
git clone https://github.com/seu-usuario/analise-precos-acoes.git

# Entre no diretório
cd analise-precos-acoes

# Crie e ative um ambiente virtual (opcional)
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Instale as dependências
pip install -r requirements.txt

# Execute o script
python sarimax_var_exogenas.py
```

## 📝 Principais Conclusões
- O modelo SARIMAX consegue capturar bem as tendências gerais dos preços das ações
- A inclusão de variáveis exógenas pode melhorar o desempenho do modelo
- É possível usar o modelo para fazer previsões de preços futuros com um erro relativamente baixo

## 🔄 Próximos Passos
- Testar outros modelos de séries temporais e comparar o desempenho
- Incluir variáveis exógenas adicionais que possam impactar os preços das ações
- Avaliar o desempenho do modelo em diferentes horizontes de previsão

## 👤 Autor
Seu Nome
- [LinkedIn](https://www.linkedin.com/in/gabrielkonno/)
- Email: gkonnoc@gmail.com

## 📜 Licença
Este projeto está sob a licença MIT - veja o arquivo LICENSE para mais detalhes.
