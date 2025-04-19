# Referências – Tabelas Auxiliares do PySUS

Esta pasta contém notebooks dedicados à exploração e mapeamento de **tabelas de referência essenciais** para o uso dos bancos de dados do SUS com a biblioteca `pysus`. São arquivos complementares, fundamentais para interpretar corretamente os códigos utilizados nas bases principais como **SIM, SIH, SIA, CNES e SINASC**.

## 📁 Notebooks disponíveis

| Arquivo | Descrição |
|--------|-----------|
| `REFERENCIAS_CBO2002_Ocupacao.ipynb` | Exploração da tabela de ocupações da CBO 2002 |
| `REFERENCIAS_CBO_tb_ocupacao_Mapeamento_Funcao.ipynb` | Função para mapear código → descrição da CBO |
| `REFERENCIAS_CID10_Categorias.ipynb` | Exploração da tabela de categorias da CID-10 |
| `REFERENCIAS_CID10_Categorias_Mapeamento_Funcao.ipynb` | Função para mapear código → descrição da CID-10 |
| `REFERENCIAS_SIGTAP_tb_procedimento.ipynb` | Exploração da tabela de procedimentos do SIGTAP |
| `REFERENCIAS_SIGTAP_tb_procedimento_Mapeamento_Funcao.ipynb` | Função para mapear código → descrição dos procedimentos do SUS |

## 🔄 Como utilizar essas funções de mapeamento

Você pode integrar as funções dos notebooks de mapeamento diretamente em seus projetos com PySUS, por exemplo:

```python
from referencias.sigtap import mapear_procedimento
descricao = mapear_procedimento('0201010012')  # Exemplo de código do SIGTAP
print(descricao)
```

> 💡 Recomendamos consolidar essas funções em um script `.py` para reaproveitamento em múltiplos notebooks.

## 🧩 Próximos passos sugeridos

- Adicionar funções de mapeamento para outras tabelas referenciais do SUS, como:
  - **CNES tipos de leitos, equipamentos e serviços**
  - **Classificações específicas do SIH e SIA**
  - **Tabela de municípios e UFs (IBGE/SUS)**

- Incluir notebooks de verificação de integridade e consistência entre códigos e suas descrições.

## 🔗 Referências externas

- [Tabela CBO 2002 - Ministério da Saúde](https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/emprego/cbo)
- [CID-10 - OMS](https://www.who.int/classifications/classification-of-diseases)
- [SIGTAP - Tabela de Procedimentos SUS](http://sigtap.datasus.gov.br)

---

Este diretório é parte do repositório [cartaproale/PySUS](https://github.com/cartaproale/PySUS), voltado à documentação prática e acessível para pesquisadores e profissionais de saúde pública.