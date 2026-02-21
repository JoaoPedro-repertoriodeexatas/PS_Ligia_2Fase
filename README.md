# 🧠 Classificação de Desinformação Digital  
### Desafio NLP – Liga Acadêmica de Inteligência Artificial (LIGIA)

## 📌 Descrição do Projeto

Este projeto tem como objetivo desenvolver um modelo supervisionado de Processamento de Linguagem Natural (NLP) para classificar textos como:

- **Informação legítima**
- **Desinformação digital**

A abordagem adotada priorizou **rigor metodológico e otimização profunda de uma estratégia clássica**, em vez de múltiplas arquiteturas complexas.

A solução final utiliza:

- TF-IDF otimizado para representação textual
- Regressão Logística com regularização L2
- Validação cruzada estratificada
- Otimização sistemática do threshold
- F1-Score como métrica principal

---

## 🎯 Estratégia Adotada

Ao invés de testar diversos algoritmos superficiais, foi escolhida uma única abordagem e realizada sua otimização completa, incluindo:

- Ajuste de hiperparâmetros do vetor TF-IDF:
  - `ngram_range=(1,2)`
  - `min_df`
  - `max_df`
  - `max_features`
  - `sublinear_tf=True`

- Ajuste da regularização da Regressão Logística (`C`)

- Validação Cruzada Estratificada (5 folds)

- Otimização do limiar de decisão (threshold search) para maximizar o F1-Score

---

## 📊 Métrica de Avaliação

A métrica principal utilizada foi:**f1_score**


Justificativa:

- O conjunto apresenta leve desbalanceamento entre classes.
- O F1-Score equilibra precisão e recall.
- É a métrica oficial do desafio.

---

## 🔍 Pipeline do Modelo

1. Análise exploratória dos dados
2. Vetorização com TF-IDF otimizado
3. Treinamento com Regressão Logística
4. Validação cruzada estratificada
5. Busca do melhor threshold
6. Avaliação final
7. Geração de arquivo de submissão

---

## 📈 Resultados

O modelo apresentou desempenho consistente em validação cruzada, com melhoria significativa após:

- Uso de n-grams
- Controle de termos raros e frequentes
- Ajuste da regularização
- Otimização do threshold

A matriz de confusão indicou boa separação entre classes, com maior dificuldade apenas em textos ambíguos.

---
## 🧩 Estrutura do Repositório

```text
.
├── notebooks/
│   ├── 01_exploracao.ipynb
│   ├── 02_modelagem_tfidf.ipynb
│   └── 03_otimizacao_threshold.ipynb
├── submission.csv
├── README.md
└── requirements.txt
```

---
## ⚙️ Ambiente

O projeto foi desenvolvido em Google Colab (Python 3.10).
As dependências estão listadas em `requirements.txt`.


---

## ⚙️ Como Executar

### 1️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

---

### 2️⃣ Executar pipeline

```bash
python src/pipeline.py

```
---

## 📂 Dados

Os arquivos `train.csv` e `test.csv` não estão incluídos neste repositório devido ao limite de tamanho do GitHub.

Para executar o projeto:

1. Baixe os dados a partir do link oficial do desafio.
2. Coloque os arquivos na pasta data com os nomes originais dos arquivos

Outra possibilidade é baixar por meio do link a seguir: [Clique aqui](https://drive.google.com/drive/folders/1ReB2ZKMnOXak-_6njUUujfnsrnTXUT1U?usp=sharing)

---

### 📦 Principais Bibliotecas Utilizadas

- scikit-learn

- pandas

- numpy

- matplotlib
---
### 🔎 Interpretabilidade

A utilização de Regressão Logística permite análise direta dos coeficientes do modelo.

Foi realizada inspeção dos termos mais relevantes para cada classe, garantindo maior transparência na tomada de decisão.
---
### ⚠️ Limitações

- Modelo baseado apenas em conteúdo textual

- Não utiliza embeddings semânticos profundos

- Sensível a reformulações linguísticas sofisticadas
---
### 🏆 Conclusão

Este projeto demonstra que uma abordagem clássica, quando cuidadosamente otimizada e validada, pode alcançar desempenho competitivo em tarefas de detecção de desinformação digital.

- A estratégia adotada priorizou:

- Rigor experimental

- Generalização

- Interpretabilidade

- Otimização da métrica-alvo
---
# 👨‍💻 Autor

João Pedro Barbosa Aragão
Liga Acadêmica de Inteligência Artificial (LIGIA)
Universidade Federal de Pernambuco
---
# 📜 Licença

Projeto desenvolvido exclusivamente para fins acadêmicos no contexto do Desafio NLP da LIGIA.
