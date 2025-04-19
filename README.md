
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

## 📁 Organização do repositório

Cada subpasta contém:

- Notebooks nomeados no padrão `SISTEMA_TABELA_ESTADO_ANO_Exploracao.ipynb`
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
  - Menu: `Ambiente de execução > Reiniciar ambiente`
  - Ou pressione: `Ctrl + M` e depois `.` (ponto)

> **ENGLISH:** After running the installation cell above, you must **restart the Google Colab runtime** to avoid compatibility errors (especially with NumPy):
> - Menu: `Runtime > Restart runtime`
> - Or press: `Ctrl + M` then `.` (dot)

---

## 💬 Contribuições

Sinta-se à vontade para propor melhorias, enviar sugestões, abrir issues ou adaptar os notebooks para sua realidade regional.

Este repositório foi organizado por **[@cartaproale](https://github.com/cartaproale)** e revisado com apoio do ChatGPT-4, com foco em acessibilidade e reprodutibilidade científica.

---

## 📚 Fontes Oficiais

- FTP do DataSUS: `ftp.datasus.gov.br`
- Repositório PySUS: [github.com/AlertaDengue/PySUS](https://github.com/AlertaDengue/PySUS)
- Tabelas auxiliares: CBO, CID-10, SIGTAP (em construção futura)
