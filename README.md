
# 🧠 PySUS – Acesso estruturado aos dados públicos do SUS

Este repositório contém notebooks interativos e validados para acesso direto e exploração de dados do **DataSUS**, por meio da biblioteca [`pysus`](https://github.com/AlertaDengue/PySUS) mantida pelo [AlertaDengue](https://info.dengue.mat.br/).

Os códigos são compatíveis com o **Google Colab** e visam facilitar o trabalho de pesquisadores, profissionais da saúde, estudantes e desenvolvedores **sem necessidade de conhecimento prévio em programação**.

> ⚠️ Este projeto é independente e não possui vínculo com o Ministério da Saúde. É mantido por voluntários com fins educacionais e científicos.

---

## 📦 Bases disponíveis e status de validação

| Sistema | Subpasta  | Status | Descrição                                      |
|---------|-----------|--------|------------------------------------------------|
| SIM     | `SIM/`    | ✅     | Sistema de Informações sobre Mortalidade       |
| SIH     | `SIH/`    | ✅     | Sistema de Informações Hospitalares do SUS     |
| SIA     | `SIA/`    | ✅     | Sistema de Informações Ambulatoriais do SUS    |
| SINASC  | `SINASC/` | ✅     | Sistema de Informações sobre Nascidos Vivos    |
| CNES    | `CNES/`   | ✅     | Cadastro Nacional de Estabelecimentos de Saúde |

> **Validados** significa que os notebooks baixam dados reais, estão organizados por estado, ano e mês, e executam com sucesso no Google Colab.

---
Cada sistema possui uma subpasta dedicada com notebooks de exploração, limpeza e mapeamento de códigos.
---

## 📁 Estrutura do Repositório

```
cartaproale/PySUS/
├── LICENSE.md
├── README.md
├── Exemplos/                       # Notebooks principais e ilustrativos
│   ├── CNES/
│   │   ├── Leitos_CNES_LT_Mapeamento_Municipios.ipynb
│   │   ├── Leitos_Por_Cidade_Top_10_Grafico.ipynb
│   │   ├── Total_Leitos_Parana_SUS_e_nao_SUS.ipynb
│   │   └── Total_Leitos_Parana.ipynb
│   ├── Mapeamento/
│   │   └── Mapeamento_IBGE_Cidades.ipynb
│   ├── SIM/
│   │   ├── SIM_CID10_Brasil_Exemplos_Exploracao.ipynb
│   │   ├── SIM_CID10_Estado_Exemplos_Exploracao.ipynb
│   │   └── SIM_CID10_Municipio_Exemplos_Exploracao.ipynb
│   └── _Iniciar/
│       ├── Iniciar_Instalacao_e_Testes_Iniciais_PySUS.ipynb
│       └── Iniciar_Teste_Instalacao_Importacao_PySUS.ipynb
│
├── Referencias/                    # Mapeamentos e tabelas de apoio
│   ├── README_referencias.md
│   ├── REFERENCIAS_CBO2002_Ocupacao.ipynb
│   ├── REFERENCIAS_CBO_tb_ocupacao_Mapeamento_Funcao.ipynb
│   ├── REFERENCIAS_CID10_Categorias.ipynb
│   ├── REFERENCIAS_CID10_Categorias_Mapeamento_Funcao.ipynb
│   ├── REFERENCIAS_SIGTAP_tb_procedimento.ipynb
│   └── REFERENCIAS_SIGTAP_tb_procedimento_Mapeamento_Funcao.ipynb
│
├── notebooks/                      # Notebooks por base e testes
│   ├── tabela_cbo.ipynb
│   ├── tabela_cid10.ipynb
│   ├── tabela_sigtap.ipynb
│   ├── Tabela_municipios.csv
│   ├── CNES/
│   │   ├── CNES_DC.ipynb
│   │   ├── CNES_EP.ipynb
│   │   ├── CNES_EQ.ipynb
│   │   ├── CNES_HB.ipynb
│   │   ├── CNES_IN.ipynb
│   │   ├── CNES_LT.ipynb
│   │   ├── CNES_PF.ipynb
│   │   ├── CNES_SR.ipynb
│   │   ├── CNES_ST.ipynb
│   │   └── README_CNES.md
│   ├── SIA/
│   │   ├── SIA_PA.ipynb
│   │   └── README_SIA.md
│   ├── SIH/
│   │   ├── SIH_CM.ipynb
│   │   ├── SIH_ER.ipynb
│   │   ├── SIH_RD.ipynb
│   │   ├── SIH_SP.ipynb
│   │   └── README_SIH.md
│   ├── SIM/
│   │   ├── SIM_CID10.ipynb
│   │   └── README_SIM.md
│   └── SINASC/
│       ├── SINASC_DN.ipynb
│       └── README_SINASC.md
│
├── tabelas/                        # Arquivos de dados auxiliares (.csv, .txt)
│   ├── cbo2002.csv
│   ├── cid10.csv
│   ├── cnes_eq.csv
│   ├── cnes_pf.csv
│   ├── cnes_st.csv
│   ├── municipios.csv
│   ├── sia_pa.csv
│   ├── sigtap_procedimentos.csv
│   ├── sih_rd.csv
│   ├── sim_cid10.csv
│   ├── sinasc_dn.csv
│   └── tb_procedimento.txt

```

---

## 🧩 Tabelas de Referência

A pasta `Referencias/` contém notebooks com funções de mapeamento para:

- **CBO** – Classificação Brasileira de Ocupações
- **CID-10** – Classificação Internacional de Doenças
- **SIGTAP** – Tabela de Procedimentos, Medicamentos e OPM do SUS

Essas funções facilitam a interpretação dos códigos presentes nos bancos de dados principais.

---

## 📁 Organização do repositório

Cada subpasta contém:

- Notebooks nomeados no padrão `SISTEMA_TABELA.ipynb`
- Um arquivo `README.md` explicando os notebooks e tabelas disponíveis
- Códigos limpos, legíveis e comentados

---

## ✨ Recomendações de uso

- Utilize o [Google Colab](https://colab.research.google.com/) para executar os notebooks sem necessidade de instalar nada.
- Sempre instale a versão atualizada do PySUS no início do notebook com:

```python
!pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
```

- 🔁 **IMPORTANTE:** Após executar o comando acima, você deve **reiniciar o ambiente do Google Colab**:
  - Menu: `Ambiente de execução > Reiniciar ambiente` ou
    Menu: `Runtime > Restart runtime`
  - Ou pressione: `Ctrl + M` e depois `.` (ponto)

---

## 💬 Contribuições

Sinta-se à vontade para propor melhorias, enviar sugestões, abrir issues ou adaptar os notebooks para sua realidade regional.

Este repositório foi organizado por **[@cartaproale](https://github.com/cartaproale)** e revisado com apoio do ChatGPT-4, com foco em acessibilidade e reprodutibilidade científica.

---

## 📚 Fontes Oficiais

- FTP do DataSUS: `ftp.datasus.gov.br`
- Repositório PySUS: [github.com/AlertaDengue/PySUS](https://github.com/AlertaDengue/PySUS)
- Tabelas auxiliares: CBO, CID-10, SIGTAP
- DATASUS – Ministério da Saúde: http://datasus.saude.gov.br/
- CID-10 – OMS: https://www.who.int/classifications/classification-of-diseases
- CBO – Ministério do Trabalho:https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/emprego/cbo
- SIGTAP – DATASUS:http://sigtap.datasus.gov.br/
