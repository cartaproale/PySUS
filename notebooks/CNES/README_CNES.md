
# 📊 CNES – Cadastro Nacional de Estabelecimentos de Saúde

Este diretório contém notebooks validados para exploração de tabelas da base **CNES** (Cadastro Nacional de Estabelecimentos de Saúde), com dados públicos do DataSUS acessados por meio da biblioteca `pysus` (mantida pelo [AlertaDengue](https://github.com/AlertaDengue/PySUS)).

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

