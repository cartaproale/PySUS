# SINASC - Sistema de Informações sobre Nascidos Vivos

Este diretório contém notebooks relacionados ao acesso e à exploração dos dados do **SINASC (Sistema de Informações sobre Nascidos Vivos)**, disponibilizados publicamente pelo DataSUS e acessados via biblioteca `pysus`, mantida pelo AlertaDengue.

---

## Notebook principal

- **`SINASC_DN.ipynb`**
  - Baixa os dados do grupo `DN` (Declaração de Nascido Vivo) para o estado do Paraná no ano de 2022.
  - Realiza uma análise exploratória dos municípios com maior número de nascimentos.
  - Gera um gráfico com os 10 municípios que registraram mais nascimentos em 2022.

---

## Como utilizar

1. Acesse o notebook diretamente pelo GitHub ou abra no Google Colab.
2. Certifique-se de executar a célula de instalação da biblioteca:

   ```python
   !pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
   ```

3. Execute as demais células passo a passo.

> 💡 **Importante**: A biblioteca `pysus` do AlertaDengue requer conversão do retorno usando `.to_dataframe()` após o `download(...)`.

---

## Grupo utilizado

- `DN`: Declaração de nascidos vivos (dados detalhados por município e unidade de saúde)

---

## Exemplo de uso

```python
from pysus.online_data.SINASC import download

df = download(states=["PR"], years=[2022], groups=["DN"]).to_dataframe()
df['CODMUNNASC'].value_counts().head(10)
```

---

## Autor

Este material faz parte do projeto [cartaproale/PySUS](https://github.com/cartaproale/PySUS), mantido por **Alexandre Kraemer**, com o objetivo de tornar acessíveis as bases públicas de dados em saúde para pesquisadores, estudantes e gestores.
