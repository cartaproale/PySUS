
# 📊 CNES – Cadastro Nacional de Estabelecimentos de Saúde

Este diretório contém notebooks validados para exploração de tabelas da base **CNES** (Cadastro Nacional de Estabelecimentos de Saúde), com dados públicos do DataSUS acessados por meio da biblioteca `pysus` (mantida pelo [AlertaDengue](https://github.com/AlertaDengue/PySUS)).

---
# PySUS CNES - Padrão de uso da função `download()`

Este documento apresenta o **padrão de uso da função `download()`** nos notebooks do módulo **CNES** da biblioteca [PySUS](https://github.com/cartaproale/PySUS), conforme validados nos notebooks oficiais.

> ⚠️ **Importante:** A função `download()` é utilizada de forma diferente dependendo do tipo da base CNES consultada. Este README consolida os dois formatos utilizados oficialmente para orientar o uso correto.

---

## 📆 Tabela de Padrões por Tipo de Base CNES

| Notebook         | Tipo de Base                 | Assinatura usada                                 | Observações                                 |
|------------------|------------------------------|--------------------------------------------------|---------------------------------------------|
| `CNES_LT.ipynb`  | Leitos hospitalares (LT)     | `download('LT', 'PR', 2023, 1).to_dataframe()`   | ✔️ Utiliza **sigla da UF** e `.to_dataframe()` |
| `CNES_ST.ipynb`  | Estabelecimentos (ST)        | `download("ST", state="41", year=2023, month=1)` | ✔️ Utiliza **código IBGE da UF**            |
| `CNES_IN.ipynb`  | Incentivos (IN)              | `download("IN", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_EQ.ipynb`  | Equipamentos (EQ)            | `download("EQ", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_HB.ipynb`  | Habilitações (HB)            | `download("HB", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_EP.ipynb`  | Equipes (EP)                 | `download("EP", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_DC.ipynb`  | Dados complementares (DC)    | `download("DC", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_PF.ipynb`  | Profissionais (PF)           | `download("PF", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |
| `CNES_SR.ipynb`  | Serviços especializados (SR) | `download("SR", state="41", year=2023, month=1)` | ✔️ Utiliza código IBGE                     |

---

## 🤔 Padrões utilizados

### 🔹 Padrão 1: Usado apenas em `CNES_LT.ipynb`
```python
from pysus.online_data.CNES import download

dados = download('LT', 'PR', 2023, 1)
df = dados.to_dataframe()
```
- Utiliza sigla da UF (ex: 'PR')
- Requer conversão com `.to_dataframe()`

### 🔹 Padrão 2: Usado nos demais notebooks CNES
```python
from pysus.online_data.CNES import download

df = download("XX", state="41", year=2023, month=1)
```
- Utiliza o código IBGE da UF (ex: 41 = Paraná)
- Retorna diretamente um DataFrame

---

## 🗂️ Códigos IBGE das Unidades Federativas

| UF | Código IBGE |
|----|-------------|
| AC | 12 |
| AL | 27 |
| AM | 13 |
| AP | 16 |
| BA | 29 |
| CE | 23 |
| DF | 53 |
| ES | 32 |
| GO | 52 |
| MA | 21 |
| MG | 31 |
| MS | 50 |
| MT | 51 |
| PA | 15 |
| PB | 25 |
| PE | 26 |
| PI | 22 |
| PR | 41 |
| RJ | 33 |
| RN | 24 |
| RO | 11 |
| RR | 14 |
| RS | 43 |
| SC | 42 |
| SE | 28 |
| SP | 35 |
| TO | 17 |

---

> Para garantir reprodutibilidade e compatibilidade com o repositório oficial, siga **exclusivamente o padrão utilizado em cada notebook correspondente**.

---

## ✅ Tabelas Validadas

Cada notebook realiza o download real dos dados da tabela correspondente para o estado do **Paraná** em **janeiro de 2023**, com análise de colunas, tipos e exemplos de valores.

| Arquivo Notebook       | Tabela | Descrição                                   |
|------------------------|--------|----------------------------------------------|
| `CNES_ST.ipynb`        | ST     | Estabelecimentos                             |
| `CNES_PF.ipynb`        | PF     | Profissionais                                |
| `CNES_SR.ipynb`        | SR     | Serviços                                     |
| `CNES_HB.ipynb`        | HB     | Habilitações                                 |
| `CNES_IN.ipynb`        | IN     | Incentivos                                   |
| `CNES_EP.ipynb`        | EP     | Estabelecimento por Procedimento             |
| `CNES_EQ.ipynb`        | EQ     | Equipamentos                                 |
| `CNES_LT.ipynb`        | LT     | Leitos                                       |
| `CNES_DC.ipynb`        | DC     | Dados Complementares                         |

---

## ⚠️ Tabela Indisponível

- `EE` – Estabelecimentos Especiais: **não está disponível via PySUS até o momento**.

---

## 📁 Organização

Cada notebook contém:
- Instalação da versão correta do `pysus`
- Download real dos dados da tabela
- Conversão para `DataFrame`
- Amostragem de colunas, tipos e exemplos

---

## 🔗 Referências

- Repositório PySUS (AlertaDengue): [https://github.com/AlertaDengue/PySUS](https://github.com/AlertaDengue/PySUS)
- Projeto cartaproale/PySUS: [https://github.com/cartaproale/PySUS](https://github.com/cartaproale/PySUS)

