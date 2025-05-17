
# Análise de Dados do SINAN (Sistema de Informação de Agravos de Notificação)

Este notebook explora os dados do **SINAN** disponíveis via biblioteca `PySUS`, com foco no estado do Paraná. O objetivo principal é demonstrar como carregar, entender e visualizar variáveis essenciais como sexo, faixa etária e distribuição geográfica dos agravos notificados.

## 📦 Dados Utilizados

- **Fonte:** Ministério da Saúde - DATASUS
- **Sistema:** SINAN – Sistema de Informação de Agravos de Notificação
- **Local:** Estado do Paraná (PR)
- **Ano:** 2023
- **Período:** Mês 1 (Janeiro)

Os dados foram obtidos diretamente via função `download()` da biblioteca `pysus.online_data.SINAN`, grupo `'AG'`.

## 🧰 Bibliotecas e Ferramentas

- `pysus` – para download dos dados
- `pandas` – manipulação tabular
- `matplotlib` e `seaborn` – visualização gráfica
- `collections.Counter` – análise frequencial
- `datetime` – tratamento de datas

## 🧪 Principais Etapas do Notebook

1. **Download e visualização da base SINAN**
   - Identificação do número de registros e colunas
   - Verificação de colunas disponíveis com `df.columns.tolist()`

2. **Análise Exploratória Inicial**
   - Contagem de linhas e colunas
   - Visualização de amostras dos dados

3. **Gráficos Gerados**
   - 📊 **Distribuição por sexo** (`CS_SEXO`)
   - 📊 **Distribuição por faixa etária** (com base em `NU_IDADE_N`)
   - (Gráficos adicionais podem ser adicionados com base nas colunas como `CS_GESTANT`, `SG_UF_NOT`, `ID_MUNICIP`, `ID_AGRAVO`, etc.)

## 📈 Sugestões de Gráficos Adicionais

Com base nas colunas disponíveis, é possível gerar gráficos para:

- Distribuição por escolaridade (`CS_ESCOL_N`)
- Agravos mais frequentes (`ID_AGRAVO`)
- Evolução temporal (`DT_NOTIFIC`, `DT_SIN_PRI`)
- Distribuição geográfica por município (`ID_MUNICIP`)
- Gestação e raça/cor (`CS_GESTANT`, `CS_RACA`)
- Proporção por UF de residência x UF de notificação (`SG_UF`, `SG_UF_NOT`)

## 📂 Organização dos Dados

Os dados possuem colunas padronizadas de notificação, como:

```python
['TP_NOT', 'ID_AGRAVO', 'DT_NOTIFIC', 'DT_SIN_PRI', 'NU_IDADE_N', 'CS_SEXO', ...]
```

O dicionário completo das colunas deve ser consultado na [documentação oficial do SINAN](https://pysus.readthedocs.io/pt/stable/), visto que o significado de algumas variáveis pode variar por tipo de agravo.

## ⚠️ Observações Importantes

- A base retorna arquivos grandes; pode ser necessário alocar mais memória ao trabalhar com anos completos.
- Os dados são pseudonimizados e públicos, mas recomenda-se seguir boas práticas de ética em pesquisa ao utilizá-los.
- As faixas etárias foram agrupadas manualmente para fins de visualização.

## 📁 Estrutura de Arquivo

O notebook faz parte do repositório [PySUS - cartaproale](https://github.com/cartaproale/PySUS) e deve ser colocado dentro da subpasta:

```
/SINAN/SINAN.ipynb
```
