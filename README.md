# PySUS – Acesso e Documentação das Bases Públicas de Saúde do Brasil 🇧🇷

Este repositório tem como objetivo facilitar o acesso, entendimento e utilização das principais **bases de dados públicas do SUS**, por meio da biblioteca [PySUS](https://github.com/AlertaDengue/PySUS), promovendo uma interface amigável e consistente para **pesquisadores leigos**, **cientistas de dados**, **gestores de saúde** e **desenvolvedores no-code/low-code**.

---

## 📊 Bases de dados documentadas

| Base | Nome Completo | Tipo | Documentação | Acesso via Notebook |
|------|----------------|------|------------------|-----------------------|
| SIM  | Sistema de Informações sobre Mortalidade | CID-10 | [`sim_cid10.csv`](tabelas/sim_cid10.csv) | [`acesso_sim.ipynb`](notebooks/acesso_sim.ipynb) |
| SIH  | Sistema de Informações Hospitalares | RD | [`sih_rd.csv`](tabelas/sih_rd.csv) | [`acesso_sih.ipynb`](notebooks/acesso_sih.ipynb) |
| CNES | Cadastro Nacional de Estabelecimentos de Saúde | ST, PF, EQ, LT, DC... | [`cnes_pf.csv`](tabelas/cnes_pf.csv) | [`acesso_cnes_st.ipynb`](notebooks/acesso_cnes_st.ipynb) |
| SINASC | Sistema de Informações sobre Nascidos Vivos | DN | [`sinasc_dn.csv`](tabelas/sinasc_dn.csv) | [`acesso_sinasc.ipynb`](notebooks/acesso_sinasc.ipynb) |
| SIA  | Sistema de Informações Ambulatoriais | PA | [`sia_pa.csv`](tabelas/sia_pa.csv) | [`acesso_sia.ipynb`](notebooks/acesso_sia.ipynb) |

---

## 🧩 Tabelas de Referência

| Tabela | Descrição | Acesso |
|--------|-----------|--------|
| CBO    | Classificação Brasileira de Ocupações | [`tabela_cbo.ipynb`](notebooks/tabela_cbo.ipynb) |
| CID-10 | Diagnósticos médicos por código | [`tabela_cid10.ipynb`](notebooks/tabela_cid10.ipynb) |
| SIGTAP | Tabela de Procedimentos SUS | [`tabela_sigtap.ipynb`](notebooks/tabela_sigtap.ipynb) |

---

## 🚀 Como utilizar no Google Colab

1. Acesse um dos arquivos `.ipynb` acima.
2. Execute a primeira célula para instalar o PySUS.
3. Reinicie o ambiente.
4. Execute o restante normalmente para carregar os dados.

---

## 👨‍🔬 Autor

**Alexandre Kraemer**  
Licença: MIT – livre para uso, modificação e distribuição.

---

## 💡 Contribuições futuras

- Inclusão de tabelas adicionais do CNES (SR, EE, GM, etc.)
- Dashboards interativos
- Integração com redes neurais no-code para previsão e agrupamento de padrões de saúde pública

