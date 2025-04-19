# 📊 PySUS – Análise de Dados do SUS com Python

Este repositório contém notebooks e utilitários para análise dos principais bancos de dados do SUS (DATASUS), incluindo:

- SIM – Sistema de Informações sobre Mortalidade
- SINASC – Sistema de Informações sobre Nascidos Vivos
- SIH – Sistema de Informações Hospitalares
- SIA – Sistema de Informações Ambulatoriais
- CNES – Cadastro Nacional de Estabelecimentos de Saúde
- Tabelas de Referência – CID-10, CBO, SIGTAP

Cada sistema possui uma subpasta dedicada com notebooks de exploração, limpeza e mapeamento de códigos.

---

## 📁 Estrutura do Repositório

```
cartaproale/PySUS/
├── CNES/
│   ├── CNES_ST_Parana_2022_Exploracao.ipynb
│   ├── CNES_PF_Parana_2022_Exploracao.ipynb
│   └── ...
├── SIM/
│   └── SIM_CID10_Parana_2022_Exploracao.ipynb
├── SIH/
│   ├── SIH_RD_Parana_2022_Exploracao.ipynb
│   ├── SIH_ER_Parana_2022_Exploracao.ipynb
│   └── ...
├── SIA/
│   └── SIA_PA_Parana_2023_Exploracao.ipynb
├── SINASC/
│   └── SINASC_DN_Parana_2022_Exploracao.ipynb
├── Referencias/
│   ├── REFERENCIAS_CBO_tb_ocupacao_Mapeamento_Funcao.ipynb
│   ├── REFERENCIAS_CID10_Categorias_Mapeamento_Funcao.ipynb
│   └── REFERENCIAS_SIGTAP_tb_procedimento_Mapeamento_Funcao.ipynb
├── README.md
└── LICENSE
```

---

## 🧩 Tabelas de Referência

A pasta `Referencias/` contém notebooks com funções de mapeamento para:

- **CBO** – Classificação Brasileira de Ocupações
- **CID-10** – Classificação Internacional de Doenças
- **SIGTAP** – Tabela de Procedimentos, Medicamentos e OPM do SUS

Essas funções facilitam a interpretação dos códigos presentes nos bancos de dados principais.

---

## 🚀 Como Utilizar

1. Clone o repositório:

   ```bash
   git clone https://github.com/cartaproale/PySUS.git
   ```

2. Instale as dependências necessárias:

   ```bash
   pip install -r requirements.txt
   ```

3. Navegue até a pasta do sistema desejado e abra o notebook correspondente.

---

## 📚 Referências Externas

- [DATASUS – Ministério da Saúde](http://datasus.saude.gov.br/)
- [CID-10 – OMS](https://www.who.int/classifications/classification-of-diseases)
- [CBO – Ministério do Trabalho](https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/emprego/cbo)
- [SIGTAP – DATASUS](http://sigtap.datasus.gov.br/)

---

Este repositório é mantido por [cartaproale](https://github.com/cartaproale) e colaboradores.