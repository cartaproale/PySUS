# SIM - Sistema de Informações sobre Mortalidade

Este diretório contém notebooks relacionados ao acesso e à exploração dos dados do **SIM (Sistema de Informações sobre Mortalidade)**, disponibilizados publicamente pelo DataSUS e acessados via biblioteca `pysus`, mantida pelo AlertaDengue.

---

## Notebook principal

- **`SIM_CID10.ipynb`**
  - Baixa os dados do grupo `CID10` (causa básica de óbito) para o estado do Paraná no ano de 2022.
  - Realiza uma análise exploratória das causas de óbito com base nos códigos CID-10.
  - Gera um gráfico de barras com as 10 causas básicas mais frequentes.

---

## Como utilizar

1. Acesse o notebook diretamente pelo GitHub ou abra no Google Colab.
2. Certifique-se de executar a célula de instalação da biblioteca:

   ```python
   !pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
   ```

3. Execute as demais células passo a passo.

> 💡 **Importante**: A biblioteca `pysus` do AlertaDengue requer conversão do resultado usando `.to_dataframe()` após o `download(...)` para acesso pleno aos dados.

---

## Grupo utilizado

- `CID10`: Base de óbitos por causa básica (classificação CID-10)

---

## Exemplo de uso

```python
from pysus.online_data.SIM import download

df = download(states=["PR"], years=[2022], groups=["CID10"]).to_dataframe()
df['CAUSABAS'].value_counts().head(10)
```

---

## Autor

Este material faz parte do projeto [cartaproale/PySUS](https://github.com/cartaproale/PySUS), mantido por **Alexandre Kraemer**, com o objetivo de tornar acessíveis as bases públicas de dados em saúde para pesquisadores, estudantes e gestores.
