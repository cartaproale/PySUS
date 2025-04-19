
# CNES — Cadastro Nacional de Estabelecimentos de Saúde

Este diretório contém notebooks validados para análise de dados da base **CNES** utilizando a biblioteca `pysus` (mantida pelo AlertaDengue). Todos os arquivos foram testados no Google Colab com dados reais e convertidos corretamente para `DataFrame`.

## ✅ Tabelas validadas

| Tabela | Descrição                                  | Notebook                          |
|--------|--------------------------------------------|-----------------------------------|
| ST     | Estabelecimentos                           | `CNES_ST_Parana_2023_Exploracao.ipynb` |
| PF     | Profissionais                               | `CNES_PF_Parana_2023_Exploracao.ipynb` |
| SR     | Serviços                                    | `CNES_SR_Parana_2023_Exploracao.ipynb` |
| HB     | Habilitações                                | `CNES_HB_Parana_2023_Exploracao.ipynb` |
| IN     | Incentivos                                  | `CNES_IN_Parana_2023_Exploracao.ipynb` |
| EP     | Estabelecimento por Procedimento            | `CNES_EP_Parana_2023_Exploracao.ipynb` |

## ℹ️ Observações

- Todas as tabelas foram extraídas para o estado do **Paraná (UF = PR)**, no mês de **Janeiro de 2023 (competência 202301)**.
- Os dados foram convertidos com `.to_dataframe()` para garantir compatibilidade com pandas.
- O notebook de cada tabela contém:
  - Instruções para instalação da biblioteca
  - Código para download dos dados
  - Primeira visualização com `.head()`
  - Mapeamento automático de colunas, tipos e exemplos

## ❌ Tabelas não disponíveis via PySUS

Durante o processo de validação, a tabela `EE` (Estabelecimentos Especiais) apresentou ausência de arquivos acessíveis no repositório FTP do DATASUS. Esta limitação será documentada no relatório final.

## 📚 Fonte

Biblioteca oficial utilizada: [`pysus`](https://github.com/AlertaDengue/PySUS)

