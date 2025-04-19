# SIA - Sistema de Informações Ambulatoriais do SUS

Este diretório contém notebooks relacionados ao acesso e à exploração dos dados do **SIA (Sistema de Informações Ambulatoriais)**, disponibilizados publicamente pelo DataSUS e acessados via biblioteca `pysus`, mantida pelo AlertaDengue.

---

## Notebook principal

- **`SIA_PA.ipynb`**
  - Baixa os dados do tipo `PA` (Produção Ambulatorial) para o estado do Paraná em janeiro de 2023.
  - Realiza uma análise exploratória dos procedimentos ambulatoriais realizados (`PA_PROC_ID`).
  - Gera um gráfico com os 10 procedimentos mais registrados.

---

## Como utilizar

1. Acesse o notebook diretamente pelo GitHub ou abra no Google Colab.
2. Certifique-se de executar a célula de instalação da biblioteca:

   ```python
   !pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
   ```

3. Execute as demais células passo a passo.

> 💡 **Importante**: A função `download(...)` exige o uso do tipo de produção (ex: `"PA"`) como último argumento, e o uso de `.to_dataframe()` para conversão.

---

## Tipo de produção utilizado

- `PA`: Produção Ambulatorial (registro consolidado por procedimentos)

---

## Exemplo de uso

```python
from pysus.online_data.SIA import download

df = download("PR", 2023, 1, "PA").to_dataframe()
df['PA_PROC_ID'].value_counts().head(10)
```

---

## Autor

Este material faz parte do projeto [cartaproale/PySUS](https://github.com/cartaproale/PySUS), mantido por **Alexandre Kraemer**, com o objetivo de tornar acessíveis as bases públicas de dados em saúde para pesquisadores, estudantes e gestores.
