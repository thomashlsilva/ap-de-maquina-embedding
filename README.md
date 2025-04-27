# Projeto de Embeddings e Representação Textual

## Descrição
Este projeto explora embeddings de palavras para processamento de linguagem natural, incluindo:
- Análise de similaridade entre palavras
- Resolução de analogias
- Representação de textos para análise de sentimentos

## Instalação
```bash
pip install -r requirements.txt
```

### Executando o Jupyter Notebook
```bash
jupyter notebook
```
Abra o notebook fornecido e execute as células conforme as instruções no arquivo.

---

## Preparação dos Dados
Baixe os embeddings e coloque na pasta `embedding_data`:
1. [Português (Glove 100d)](http://143.107.183.175:22980/download.php?file=embeddings/glove/glove_s100.zip) - renomeie para `glove.pt.100.txt`
2. [Inglês (Glove 100d)](http://nlp.stanford.edu/data/glove.6B.zip) - use o arquivo `glove.6B.100d.txt` renomeado para `glove.en.100.txt`

## Funcionalidades Principais

### 1. Visualização de Embeddings
```python
from embeddings.utils import plot_words_embeddings
plot_words_embeddings(embedding_dict, ["rei", "rainha", "homem", "mulher"])
```

### 2. Resolução de Analogias
```python
analogy_solver.analogia("homem", "mulher", "rei")  # Retorna "rainha"
```

### 3. Métodos de Representação
- **Bag of Words**: Contagem de palavras
- **Média de Embeddings**: Soma vetorial das palavras

### 4. Avaliação de Métodos
Comparação de técnicas para classificação de sentimentos em reviews da Amazon.

## Resultados
O método Bag of Words obteve melhor desempenho (F1-macro: 0.85) nas avaliações.

## Referências
- Hartmann et al. (2017) - Embeddings em Português
- Pennington et al. (2015) - Modelo GloVe

## Créditos

Atividade desenvolvida para a disciplina de Machine Learning do CEFET-MG, Campus Nova Gameleira.

Material baseado nas aulas do professor Daniel Hasan Dalip.