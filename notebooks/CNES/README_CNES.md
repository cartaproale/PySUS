# CNES - Cadastro Nacional de Estabelecimentos de Saúde

Este diretório contém notebooks relacionados ao acesso e à exploração dos dados do **CNES (Cadastro Nacional de Estabelecimentos de Saúde)**, disponibilizados publicamente pelo DataSUS e acessados via biblioteca `pysus`, mantida pelo AlertaDengue.

---

## Notebook principal

- **`CNES_ST_PR_2023_Exploracao_Oficial.ipynb`**
  - Baixa os dados da tabela `ST` (Estabelecimentos) para o estado do Paraná em janeiro de 2023.
  - Realiza uma análise exploratória do tipo de unidade (`TP_UNID`) dos estabelecimentos.
  - Gera um gráfico com os tipos de unidade mais frequentes cadastrados no CNES.

---

## Como utilizar

1. Acesse o notebook diretamente pelo GitHub ou abra no Google Colab.
2. Certifique-se de executar a célula de instalação da biblioteca:

   ```python
   !pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
   ```

3. Execute as demais células passo a passo.

> 💡 **Importante**: A função `download(...)` do CNES requer como primeiro argumento o nome da tabela (`"ST"`, `"LT"`, `"EQ"`, etc.).

---

## Tabela utilizada

- `ST`: Cadastro principal de estabelecimentos de saúde

---

## Exemplo de uso

```python
from pysus.online_data.CNES import download

df = download("ST", "PR", 2023, 1).to_dataframe()
df['TP_UNID'].value_counts().head(10)
```

---

## Autor

Este material faz parte do projeto [cartaproale/PySUS](https://github.com/cartaproale/PySUS), mantido por **Alexandre Kraemer**, com o objetivo de tornar acessíveis as bases públicas de dados em saúde para pesquisadores, estudantes e gestores.
