# PySUS (cartaproale)

Este repositório tem como objetivo fornecer **exemplos práticos e notebooks funcionais** para acesso, leitura e exploração de dados públicos de saúde do SUS por meio da biblioteca `pysus` mantida pelo [AlertaDengue](https://github.com/AlertaDengue/PySUS).

Ele foi reorganizado para facilitar a navegação por sistema de informação (SIM, SIH, SINASC, SIA, CNES), com foco na compatibilidade com o Google Colab e na acessibilidade para pesquisadores e desenvolvedores.

---

## ✅ Bases atualizadas e testadas

As seguintes bases já possuem notebooks validados e revisados:

| Sistema | Tópico                         | Arquivo notebook                                 |
|---------|--------------------------------|--------------------------------------------------|
| SIM     | Causas de óbito (CID10)        | `notebooks/SIM/SIM_CID10_PR_2022_Exploracao.ipynb` |
| SIH     | Internações hospitalares (RD)  | `notebooks/SIH/SIH_RD_PR_2023_Exploracao_Oficial.ipynb` |
| CNES    | Estabelecimentos (ST)          | `notebooks/CNES/CNES_ST_PR_2023_Exploracao_Oficial.ipynb` |
| SINASC  | Nascidos vivos (DN)            | `notebooks/SINASC/SINASC_DN_PR_2022_Exploracao.ipynb` |
| SIA     | Produção ambulatorial (PA)     | `notebooks/SIA/SIA_PA_PR_2023_Exploracao_Oficial.ipynb` |

---

## 📂 Organização do repositório

- `notebooks/`: Contém os exemplos separados por sistema
- `README.md` em cada subpasta: explica como usar o notebook específico
- `scripts/`, `documentacao/` ou outros diretórios existentes: **podem conter partes ainda úteis da versão original do repositório**, especialmente para usuários avançados

> ⚠️ **Atenção**: Este repositório está passando por um processo de validação completa. Apenas os notebooks listados acima estão garantidamente atualizados com a versão do `pysus` do AlertaDengue.

---

## 📌 Requisitos

- Python 3.8 ou superior
- Biblioteca `pysus` atualizada:

```python
!pip install git+https://github.com/AlertaDengue/PySUS.git --upgrade
```

---

## 🙋‍♂️ Autor

Este projeto é mantido por **Alexandre Kraemer** com o objetivo de democratizar o acesso a dados públicos de saúde e auxiliar pesquisadores, estudantes e gestores no uso da biblioteca PySUS com segurança e confiabilidade.

Contribuições são bem-vindas!

[Repositório GitHub](https://github.com/cartaproale/PySUS)
