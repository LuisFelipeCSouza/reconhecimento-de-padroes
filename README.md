# Reconhecimento de Padrões (TPH8213) - Trabalho Prático 1

Repositório destinado aos códigos, análises e relatório do trabalho prático da disciplina de Reconhecimento de Padrões (TPH8213) do Programa de Pós-Graduação em Engenharia Elétrica (PPGEE) da Universidade Federal do Ceará (UFC).

**Autor:** Luis Felipe Carneiro de Souza (Matrícula: 593034)  
**Grupo de Pesquisa:** Grupo de Redes Elétricas Inteligentes (GREI)  
**Professor:** Prof. Dr. Guilherme Barreto  
**Local:** Fortaleza, Ceará

---

## 📌 Sobre o Projeto
Este projeto tem como objetivo a implementação do zero e a avaliação de desempenho de classificadores fundamentais de reconhecimento de padrões baseados em distância e correlação. O desenvolvimento foi realizado na linguagem Python, com foco na manipulação de matrizes, cálculo de métricas (Acurácia, Matrizes de Confusão) e geração de gráficos com qualidade de publicação para o relatório técnico.

## 🚀 Classificadores Implementados
Os algoritmos a seguir foram implementados teoricamente e aplicados ao conjunto de dados:
* **Vizinho Mais Próximo (1-NN):** Busca baseada na minimização da distância para amostras individuais.
* **Centróide Mais Próximo (MDC):** Classificação baseada na menor distância Euclidiana para o vetor médio de cada classe.
* **MDC Robusto a Outliers:** Variação utilizando o vetor mediano da classe e a distância Quarteirão (Norma L1).
* **Máxima Correlação:** Atribuição baseada no maior produto interno entre vetores de norma unitária (amostra de teste e centróide).

## 📂 Estrutura do Repositório
* `/graficos/`: Contém todas as figuras geradas pelos códigos em formato `.pdf` (Matrizes de confusão, gráficos de dispersão, etc.).
* `/relatorio/`: Contém os arquivos e o código-fonte em LaTeX (`documento.tex`, `ref.bib`) referentes à documentação do trabalho.
* `/notebooks/` (ou a raiz do projeto): Arquivos `.ipynb` contendo a rotina de pré-processamento, implementação matemática dos classificadores e rotinas de plotagem.

## 🛠️ Tecnologias e Dependências
* **Linguagem:** Python 3.x
* **Principais Bibliotecas:** `numpy`, `pandas`, `matplotlib`, `seaborn`
* **Documentação:** LaTeX (compilado via `pdflatex`)

## ⚙️ Como Executar
1. Clone este repositório para a sua máquina local:
   ```bash
   git clone [https://github.com/LuisFelipeCSouza/reconhecimento-de-padroes.git](https://github.com/LuisFelipeCSouza/reconhecimento-de-padroes.git)

## ⚙️ Como Executar

Este projeto utiliza o [uv](https://github.com/astral-sh/uv) da Astral como gerenciador de pacotes e ambientes virtuais, garantindo uma instalação reprodutível e extremamente rápida das dependências.

1. Certifique-se de ter o `uv` instalado em sua máquina. Caso não tenha, consulte o guia de instalação na [documentação oficial](https://docs.astral.sh/uv/).
2. Clone este repositório para a sua máquina local e acesse a pasta do projeto:
   ```bash
   git clone [https://github.com/LuisFelipeCSouza/reconhecimento-de-padroes.git](https://github.com/LuisFelipeCSouza/reconhecimento-de-padroes.git)
   cd reconhecimento-de-padroes

3. Sincronize o projeto. Este comando criará automaticamente um ambiente virtual (.venv) e instalará todas as dependências com as versões exatas utilizadas no desenvolvimento:

    ```Bash
    uv sync
    ```