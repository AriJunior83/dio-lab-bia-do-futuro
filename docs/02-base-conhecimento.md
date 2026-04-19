# Base de Conhecimento

## Dados Utilizados

| Arquivo | Formato | Para que serve o Ari |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores e entender necessidade dos Clientes |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

[Sua descrição aqui]

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

```Python

import pandas as pd
import json

# CSVs
historico = pd.read_csv('data/historico_atendimento.csv')
transacoes = pd.read_csv('data/transacoes.csv')

# JSONs
with open('data/perfil_investidor.json', 'r', encoding='utf-8') as f:
    perfil = json.load(f)

with open('data/produtos_fina
```

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

[Sua descrição aqui]

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
