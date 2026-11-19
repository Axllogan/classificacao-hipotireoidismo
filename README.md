# Classificação binária com Machine Learning

Projeto desenvolvido como trabalho de conclusão de curso em Ciência de Dados.

## Objetivo

O objetivo deste trabalho é utilizar técnicas de Machine Learning para classificar registros de uma base de dados relacionada à tireoide.

A variável-alvo é `binaryClass`, composta pelas classes P e N. A classe N é minoritária e foi utilizada como classe positiva na avaliação dos modelos.

## Base de dados

A base original possui 3.772 registros. Após a remoção de 61 duplicatas, foram utilizados 3.711 registros:

- Classe P: 3.420 registros.
- Classe N: 291 registros.

Foram analisadas variáveis como idade, sexo e exames laboratoriais, incluindo TSH, T3, TT4, T4U e FTI.

## Etapas do projeto

1. Leitura e limpeza dos dados.
2. Análise exploratória.
3. Tratamento de valores ausentes e preparação das variáveis.
4. Separação entre treinamento e teste.
5. Treinamento e comparação dos modelos.
6. Avaliação dos resultados e análise dos erros.

## Modelos utilizados

Foram comparados três modelos:

- Dummy Classifier.
- Regressão logística.
- Árvore de decisão.

A escolha do modelo principal foi realizada com validação cruzada estratificada.

## Resultados

A árvore de decisão apresentou o melhor resultado na validação cruzada e foi escolhida como modelo principal.

No conjunto de teste, apresentou:

| Métrica | Resultado |
|---|---|
| Acurácia | 97,8% |
| Recall da classe N | 98,6% |
| Precisão da classe N | 79,1% |
| Average Precision | 0,867 |

Dos 73 registros da classe N presentes no teste, 72 foram classificados corretamente.

## Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Arquivos do projeto

- `Trabalho_Hipotireoidismo.ipynb`: notebook com os códigos, gráficos, análises e conclusões.
- `Base_M43_Pratique_Hypothyroid.csv`: base de dados utilizada no projeto.
- `requirements.txt`: bibliotecas necessárias para executar o notebook.

## Como executar

1. Baixe os arquivos do repositório.
2. Mantenha o notebook e o CSV na mesma pasta.
3. Instale as bibliotecas listadas em `requirements.txt`.
4. Abra o notebook no Jupyter.
5. Execute as células na ordem apresentada.

## Limitações

A base apresenta desbalanceamento entre as classes e quantidade limitada de registros N. Os resultados foram obtidos com essa base e precisam de validação adicional antes de qualquer aplicação externa.

O modelo não deve ser utilizado como ferramenta de diagnóstico clínico sem avaliação profissional.
