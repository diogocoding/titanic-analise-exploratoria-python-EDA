# titanic-analise-exploratoria-python-EDA
Análise Exploratória de Dados do Titanic com Python. Foco em tratamento, padronização e visualização de dados para identificar fatores de sobrevivência.
---# 🚢 Análise Exploratória de Dados - Titanic

## 🧾 Sobre o Projeto

Este projeto consiste em uma **Análise Exploratória de Dados (EDA)** completa do famoso conjunto de dados do Titanic. O objetivo é realizar um processo de tratamento e limpeza dos dados para, em seguida, aplicar técnicas de visualização e estatística a fim de responder à pergunta central:

> **"O que influenciou a sobrevivência dos passageiros no naufrágio do Titanic?"**

Este notebook documenta cada passo, desde a importação dos dados brutos até a conclusão final sobre os fatores que mais impactaram as chances de sobrevivência.

---

## 🛠️ Metodologia e Etapas

O projeto foi estruturado seguindo as principais etapas de um pipeline de análise de dados:

1.  **Carregamento e Inspeção Inicial:** Primeiro contato com os dados para entender sua estrutura, tipos e a presença de valores ausentes.

2.  **Limpeza e Tratamento de Dados:**
    * Tratamento de valores nulos nas colunas `Age`, `Embarked` e `Cabin`, utilizando estratégias como substituição pela mediana e moda.
    * Remoção de colunas com excesso de dados faltantes (`Cabin`).

3.  **Engenharia de Atributos:**
    * Conversão de variáveis categóricas em numéricas (`Sex`, `Embarked`) para que possam ser utilizadas em análises estatísticas.

4.  **Padronização dos Dados:**
    * Aplicação do `StandardScaler` do Scikit-learn para colocar todas as variáveis numéricas na mesma escala, evitando que características com valores maiores dominem a análise.

5.  **Análise Exploratória e Visualização:**
    * Cálculo de métricas de centralidade e dispersão (média, mediana, desvio padrão).
    * Criação de gráficos para visualizar a distribuição dos dados (histogramas, boxplots).
    * Análise da relação entre cada variável e a taxa de sobrevivência, com foco em:
        * **Gênero:** Qual a diferença na sobrevivência entre homens e mulheres?
        * **Classe Socioeconômica:** A classe do ticket influenciou?
        * **Idade:** Crianças tiveram mais chances?
        * **Tamanho da Família:** Viajar sozinho ou em grupo fez diferença?
    * Investigação de **outliers** para entender o comportamento de passageiros com características extremas (tarifas muito altas, famílias muito grandes, etc.).

---

## ✨ Principais Conclusões

A análise revelou que a sobrevivência não foi aleatória, mas sim fortemente influenciada por uma clara hierarquia social:

* **Gênero:** Ser mulher foi o fator isolado com maior impacto positivo na sobrevivência (taxa de ~74%).
* **Classe Social:** Passageiros da Primeira Classe (com as tarifas mais altas) tiveram uma chance de sobreviver significativamente maior (~72% para outliers de tarifa).
* **Idade:** Ser criança (0-12 anos) aumentou as chances de sobrevivência (~58%).
* **Tamanho da Família:** Viajar em famílias muito grandes foi um fator de risco, diminuindo a chance de sobrevivência.

---

## 🚀 Ferramentas Utilizadas

* **Linguagem:** Python
* **Bibliotecas:**
    * `Pandas` para manipulação e tratamento dos dados.
    * `Matplotlib` e `Seaborn` para visualização de dados.
    * `Scikit-learn` para pré-processamento (`StandardScaler`).
* **Ambiente:** Google Colab
