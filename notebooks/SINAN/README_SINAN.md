
# 🧪 Notebooks — Base SINAN (Sistema de Informação de Agravos de Notificação)

Esta pasta contém notebooks interativos de exploração e análise de dados do **SINAN**, utilizando exclusivamente a biblioteca [PySUS](https://pysus.readthedocs.io/pt/stable/).

Todos os exemplos são compatíveis com o Google Colab e seguem as diretrizes padronizadas do projeto **PySUS Assistente No-Code** para profissionais de saúde pública, epidemiologistas e pesquisadores.

---

## 📁 Conteúdo

| Notebook | Descrição |
|----------|-----------|
| [`SINAN.ipynb`](SINAN.ipynb) | Exemplo geral de download, visualização e inspeção de dados do SINAN por UF e ano |
| [`SINAN_Dengue.ipynb`](SINAN_Dengue.ipynb) | Análise específica dos casos de Dengue, com filtros, estatísticas e agrupamentos |
| [`SINAN_Leptospirose.ipynb`](SINAN_Leptospirose.ipynb) | Análise de casos de Leptospirose, incluindo faixas etárias e distribuição temporal |

---

## ✅ Requisitos

Antes de executar os notebooks, instale a versão mais recente da biblioteca:

```python
!pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
```

E reinicie o ambiente de execução no Colab após a instalação.

---

## 📊 Funcionalidades Demonstradas

- Acesso direto a dados públicos do DATASUS (SINAN)
- Cálculo da idade a partir das datas (ou ano) de nascimento
- Geração de faixas etárias padronizadas
- Análises por UF, agravo e ano
- Visualização com gráficos de barras e séries temporais
- Manipulação segura de dados faltantes e inconsistentes

---

## 🧠 Público-alvo

Estes notebooks foram desenvolvidos para apoiar:

- Pesquisadores em epidemiologia
- Profissionais de vigilância em saúde
- Técnicos de análise em secretarias municipais e estaduais
- Estudantes de graduação, mestrado e doutorado em Saúde Coletiva e áreas correlatas

---

## 📌 Observação

Todas as análises são feitas diretamente a partir dos dados públicos do DATASUS e não requerem acesso a dados sensíveis. Os notebooks foram validados para uso educativo e técnico.

---

## 📬 Dúvidas ou contribuições?

Abra uma [issue](https://github.com/cartaproale/PySUS/issues) ou envie um pull request!
