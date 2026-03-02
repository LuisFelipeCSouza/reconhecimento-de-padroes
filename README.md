# Reconhecimento de Padrões (TPH8213) - Trabalho Prático 1

Repositório destinado aos códigos, análises e relatório do trabalho prático da disciplina de Reconhecimento de Padrões (TPH8311) do Programa de Pós-Graduação em Engenharia Elétrica (PPGEE) da Universidade Federal do Ceará (UFC).

**Autor:** Luis Felipe Carneiro de Souza (Matrícula: 593034)  
**Grupo de Pesquisa:** Grupo de Redes Elétricas Inteligentes (GREI)  
**Professor:** Prof. Dr. Guilherme Barreto  
**Local:** Fortaleza, Ceará

---

## 📌 Sobre o Repositório

Este projeto compila a implementação do zero, avaliação de desempenho e análise de viabilidade numérica de diversos métodos clássicos de classificação de padrões e processamento de dados. O desenvolvimento é dividido em três frentes principais de estudo, focando em métricas de distância, estimação de matrizes de covariância e redução de dimensionalidade.

## 📂 Estrutura dos Trabalhos

### TC 1: Classificadores Baseados em Distância e Correlação

Aborda o problema de classificação de patologias da coluna vertebral (3 classes) , utilizando o banco de dados *Vertebral Column* da UCI.

* **Modelos Implementados:** Classificador Vizinho Mais Próximo (com distância de Minkowski de diversas ordens), Distância Mínima ao Centróide (tradicional e versão robusta a *outliers*), e Classificador de Máxima Correlação.
* **Avaliação:** Análise de desempenho computacional (tempos de treinamento e teste) e estatística ao longo de 100 rodadas independentes (acurácia média, desvio-padrão, máxima, mínima e mediana).
* **Experimentos:** Extração de matrizes de confusão e avaliação do impacto da variação percentual na separação de treino e teste (ex: 20/80, 50/50, 80/20).

### TC 2: Estimação e Inversão de Matrizes de Covariância

Focado na estimação da matriz de covariância global e por classes, utilizando o conjunto *Wall-Following Robot Navigation* (4 e 24 sensores).

* **Análise de Desempenho:** Comparação sistemática e científica do tempo de execução de 4 métodos algorítmicos implementados contra a função nativa da linguagem, avaliada via histogramas e *violin plots* após 100 rodadas.
* **Métricas:** Cálculo da norma da matriz de diferenças para validar a acurácia da estimação.
* **Viabilidade Numérica:** Avaliação da invertibilidade das matrizes através do posto e do número de condicionamento. Aplicação de técnicas de regularização para matrizes mal-condicionadas durante a etapa de inversão.

### TC 3: Redução de Dimensionalidade e Clusterização

Expande a análise dos dados do robô navegador (24 sensores), introduzindo transformações no espaço de atributos.

* **Modelos Implementados:** Classificador Quadrático Gaussiano (CQG) e Classificador de Distância Mínima ao Protótipo (DMP, baseado no algoritmo K-médias aplicado a cada classe).
* **Análise de Componentes Principais (PCA):** Determinação do número ideal de componentes ($q$) através do gráfico da variância explicada, visando reduzir a dimensão sem degradar os modelos.
* **Avaliação Integrada:** Comparativo rigoroso (média e desvio padrão global e por classe) do desempenho dos classificadores treinados com os dados brutos *versus* dados transformados por PCA.

## 🛠️ Tecnologias e Dependências

* **Linguagem:** Python 3.x
* **Principais Bibliotecas:** `numpy`, `pandas`, `matplotlib`

## ⚙️ Como Executar

Este projeto utiliza o [uv](https://github.com/astral-sh/uv) da Astral como gerenciador de pacotes e ambientes virtuais, garantindo uma instalação reprodutível e extremamente rápida das dependências.

1. Certifique-se de ter o `uv` instalado em sua máquina. Caso não tenha, consulte o guia de instalação na [documentação oficial](https://docs.astral.sh/uv/).
2. Clone este repositório para a sua máquina local e acesse a pasta do projeto:

   ```bash
   git clone "https://github.com/LuisFelipeCSouza/reconhecimento-de-padroes.git"
   cd reconhecimento-de-padroes
   ```

3. Sincronize o projeto. Este comando criará automaticamente um ambiente virtual (.venv) e instalará todas as dependências com as versões exatas utilizadas no desenvolvimento:

    ```Bash
    uv sync
    ```
