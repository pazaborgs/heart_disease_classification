# Classificador de Risco de Doença Cardíaca 🫀

Este repositório apresenta um projeto originalmente desenvolvido como parte do Projeto Integrador IV do curso de Ciência de Dados da UNIVESP, durante o segundo semestre de 2024. Na ocasião, o resultado não atingiu o desempenho esperado. Agora, retomo o projeto com uma nova perspectiva, aplicando um pipeline mais estruturado, código revisado e uma abordagem binária para o problema, utilizando tanto redes neurais quanto regressão logística para comparação de desempenho.

## Observações

* Apesar de ter sido um projeto em grupo, a maior parte da análise, desenvolvimento de código e redação foi conduzida por mim, devido a dificuldades de continuidade por parte dos demais integrantes. A publicação deste repositório tem como objetivo compartilhar o aprendizado técnico e a aplicação prática dos conceitos de ciência de dados em um contexto do mundo real.
* Este projeto foi realizado em um contexto acadêmico. Os nomes de instituições de saúde e integrantes do grupo foram omitidos por motivos de privacidade e ética, e por não haver confirmação de permissão para divulgação pública fora do ambiente universitário.

## Objetivo do Projeto

O objetivo principal deste projeto é desenvolver uma rede neural para a classificação do risco de doença cardíaca, utilizando o conjunto de dados Heart Disease da UCI. Além disso, o projeto inclui um dashboard interativo que auxilia na Análise Exploratória de Dados (EDA) e na visualização de informações relevantes sobre o dataset.

## Sobre o Conjunto de Dados

O Heart Disease Dataset do UCI Machine Learning Repository contém dados clínicos utilizados para a predição da presença de doença cardíaca em pacientes. O conjunto inclui variáveis demográficas, históricos médicos e resultados de exames físicos e laboratoriais. O conjunto completo tem 76 atributos, mas todos os experimentos publicados citam ter utilizado um subconjunto com apenas 14 deles. O presente projeto também usa somente esses 14 atributos.

Autores do Dataset:

* Andras Janosi;
* Wolfgang Steinbrunn;
* Martin Pfisterer; e
* Robert Detrano.

**Referência do Dataset:**
Janosi, A., Steinbrunn, W., Pfisterer, M., & Detrano, R. (1989). Heart Disease Dataset. UCI Machine Learning Repository.
https://doi.org/10.24432/C52P4X

## Sobre esse Notebook

Em 2024, utilizei o Heart Disease Dataset da UCI para desenvolver uma rede neural capaz de prever o risco de doenças cardíacas. Esse modelo foi desenvolvido como parte do Projeto Integrador IV da Universidade Virtual do Estado de São Paulo (UNIVESP). Durante o processo, retornei a um posto de saúde da minha cidade — onde já havia trabalhado anteriormente — para dialogar com os profissionais da área sobre o uso de aprendizado de máquina na saúde. As conversas com a equipe local foram fundamentais: além de fornecerem insights práticos e inspiração, também contribuíram para ancorar o projeto em um contexto realista e relevante.

Além do modelo, desenvolvi um painel interativo em Plotly para explorar as variáveis do conjunto de dados e comunicar os principais insights à comunidade envolvida. Realizei todo o desenvolvimento do projeto individualmente. Embora o relatório final inclua o nome de outro integrante, este se desvinculou do trabalho ainda na metade do percurso.

Algum tempo depois, retomei o projeto com o objetivo de refatorar o código, melhorar a explicação dos métodos utilizados e aplicar abordagens mais apropriadas ao problema. Uma das principais mudanças foi a implementação de um modelo de regressão logística, mais adequado ao cenário de classificação multiclasse presente no conjunto de dados.

Na versão inicial, forcei a aplicação de uma rede neural, mesmo com limitações que comprometiam sua performance. Entre os principais problemas encontrados, destaco:

* Tamanho reduzido do dataset: com cerca de 300 amostras, o volume de dados era insuficiente para treinar uma rede neural com bom desempenho, resultando em acurácias entre 60% e 70%. Além disso, modelos mais complexos sofriam rapidamente com overfitting.
* Separabilidade linear das variáveis: a análise exploratória de dados (EDA) indicava que muitas das variáveis quantitativas apresentavam separação razoavelmente linear entre as classes, o que favorece modelos como a regressão logística. Isso também foi confirmado empiricamente pelos resultados obtidos com classificadores lineares.

Com a retomada do projeto, pude revisar o pipeline de pré-processamento, aplicar validações mais robustas e, para o caso da rede neural, reformular o problema como uma tarefa de classificação binária. Essa mudança resultou em um modelo mais estável e com desempenho significativamente superior ao original.

* Nota 2: Refatorar o projeto é o principal responsável pelas diferenças que vão existir entre a documentação feita na época e o presente projeto apresentado.

## 📊 Etapas do Projeto

* Análise Exploratória de Dados (EDA): desenvolvimento de um dashboard interativo com Plotly e Dash para análise visual.
* Modelagem Preditiva: construção, treino e avaliação de uma rede neural com Keras/TensorFlow.

## Tecnologias Utilizadas

- Python.
- Bibliotecas: Pandas, Plotly, Dash, Scikit-learn, Keras, TensorFlow.
- Jupyter Notebooks.

---

# Como Executar

1. Clone o repositório

```bash
git clone https://github.com/pazaborgs/heart_disease_classification.git
cd seu-repositorio
```

2. Crie um ambiente virtual (opcional)

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

3. Instale as dependências

```bash
pip install -r requirements.txt
```

4. Execute os notebooks

```bash
jupyter notebook
```

Pode-se rodar os notebooks também no Colab ou ferramenta similiar.







