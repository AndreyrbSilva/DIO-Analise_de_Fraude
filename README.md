# Detecção de Fraudes em Transações Financeiras

Projeto desenvolvido como entrega do bootcamp Python para Análise e Automação de Dados da DIO em parceria com a Accenture.

## Objetivo

Identificar padrões suspeitos em transações financeiras usando análise exploratória de dados e regras de detecção baseadas em heurística.

## Tecnologias

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Pytest
- Google Colab

## Estrutura do projeto

```
├── DesafioDio_DeteccaoFraudes.ipynb
└── README.md
```

## O que foi feito

**Análise exploratória**
- Proporção de fraudes no dataset
- Taxa de fraude por canal de pagamento
- Distribuição de valores entre transações normais e fraudulentas
- Localizações com maior incidência de fraude

**Feature engineering**
- Extração de hora do dia a partir do timestamp
- Contagem de transações por cliente

**Padrão identificado: card testing**
- Clientes realizaram microtransações (R$2 a R$4) segundos antes de uma compra de alto valor
- Padrão real usado por fraudadores para validar cartões antes de usá-los

**Regras de detecção**
- Valor acima de R$5.000
- Transação entre 0h e 4h59
- Localização internacional identificada no dataset

**Testes automatizados**
- 6 casos de teste com Pytest cobrindo valor alto, madrugada, localização suspeita e transação normal

## Como executar

Abra o notebook no Google Colab e execute as células em ordem. Nenhuma dependência externa precisa ser instalada além do pytest, que é instalado dentro do próprio notebook.
