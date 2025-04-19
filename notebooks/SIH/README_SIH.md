
# SIH — Sistema de Informações Hospitalares (DATASUS)

Esta pasta contém notebooks atualizados para análise de dados do **SIH/SUS**, utilizando a biblioteca `pysus` (AlertaDengue). Os notebooks foram testados e validados com dados reais no Google Colab.

## ✅ Notebooks validados

| Tipo de dado | Descrição                              | Notebook                                |
|--------------|----------------------------------------|-----------------------------------------|
| RD           | Registros de Internações               | `SIH_RD.ipynb` |
| SP           | Serviços Profissionais                 | `SIH_SP.ipynb`         |
| ER           | Emergência Referenciada                | `SIH_ER.ipynb`         |
| CM           | Cirurgias Ambulatoriais                | `SIH_CM.ipynb`         |

> ℹ️ O notebook `SIH_CM.ipynb` utiliza um recorte de 2 arquivos do ano de 2019 para evitar erros de timeout e garantir testagem funcional.

## 🔧 Estrutura dos notebooks

Cada notebook segue a estrutura:
- Instalação da biblioteca PySUS
- Importação dos módulos necessários
- Download dos dados diretamente dos servidores oficiais
- Conversão dos dados para `pandas.DataFrame`
- Mapeamento de colunas, tipos e exemplos de valores

## 🧪 Status da validação

- Apenas os notebooks listados acima foram validados com sucesso.
- A instrução `.to_dataframe()` foi incluída após o `download(...)` para evitar erros comuns de tipo `ParquetSet`.

## 📦 Fonte

Biblioteca oficial utilizada: [`pysus`](https://github.com/AlertaDengue/PySUS)
