
# 📂 Dicionário de Dados

Este diretório contém as bases de dados utilizadas para a análise econométrica e de NLP do projeto.

## 1. Base Primária (NLP)
| Arquivo | Descrição | Período | Formato |
| :--- | :--- | :--- | :--- |
| **`discursos_senado_imperio_1826_1888.parquet`** | Base consolidada com discursos brutos e lematizados, oradores e metadados políticos. | 1826-1888 | Parquet (GZIP) |

## 2. Bases Econômicas (Séries Históricas)
| Arquivo | Variáveis Principais | Fonte/Autor |
| :--- | :--- | :--- |
| **`dados_escravidao_pedro_mello.csv`** | Preço médio de venda e aluguel de escravizados (RJ/SP). | **Pedro Mello** (Estatísticas Históricas) |
| **`dados_economicos_cafe.csv`** | Preço da saca de café (Cotação internacional e local). | IPEADATA / Fontes Históricas |
| **`dados_cambio_historico.csv`** | Taxa de Câmbio (Réis/Libra Esterlina). | IPEADATA |
| **`dados_risk_free_summerhill_2015.csv`** | Taxa de juros de títulos soberanos brasileiros (Yields). | **William Summerhill** (2015) |
| **`dados_historicos_eulalia_lobo.csv`** | Índices de custo de vida e salários no Rio de Janeiro. | **Eulália Lobo** |
| **`dados_monetarios_m1_pelaez_suzigan.csv`** | Agregados monetários (M1 - Meios de Pagamento). | **Peláez & Suzigan** |

---
*Nota: Todas as bases econômicas foram normalizadas para facilitar o merge com a base de discursos pelo ano.*
