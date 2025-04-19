# SIH - Sistema de Informações Hospitalares

Este diretório contém notebooks relacionados ao acesso e à exploração dos dados do **SIH (Sistema de Informações Hospitalares)**, disponibilizados publicamente pelo DataSUS e acessados via biblioteca `pysus`, mantida pelo AlertaDengue.

---

## Notebook principal

- **`SIH_RD_PR_2023_Exploracao_Oficial.ipynb`**
  - Baixa os dados do tipo `RD` (Registro de internações) para o estado do Paraná no mês de janeiro de 2023.
  - Realiza uma análise exploratória dos diagnósticos principais (CID-10).
  - Gera um gráfico de barras com os 10 diagnósticos de internação mais frequentes.

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

## Tipo de produção utilizado

- `RD`: Registros de internações hospitalares (Resumo de AIH)

---

## Exemplo de uso

```python
from pysus.online_data.SIH import download

df = download("PR", 2023, 1, "RD").to_dataframe()
df['DIAG_PRINC'].value_counts().head(10)
```

---

## Autor

Este material faz parte do projeto [cartaproale/PySUS](https://github.com/cartaproale/PySUS), mantido por **Alexandre Kraemer**, com o objetivo de tornar acessíveis as bases públicas de dados em saúde para pesquisadores, estudantes e gestores.
