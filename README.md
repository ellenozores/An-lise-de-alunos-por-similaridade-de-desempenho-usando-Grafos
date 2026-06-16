# 🎓 Rede de Alunos por Similaridade de Desempenho

## 📌 Sobre o Projeto

Este projeto aplica conceitos de Análise de Redes (Grafos) para identificar padrões de desempenho acadêmico entre estudantes.

Utilizando o dataset Student Performance Dataset, foi construída uma rede onde cada nó representa um aluno e as conexões representam similaridade entre características acadêmicas e comportamentais.

O objetivo foi investigar como fatores como histórico de notas, reprovações, faltas e hábitos dos estudantes influenciam a formação de grupos com desempenhos semelhantes.

---

## 🎯 Objetivos

* Construir uma rede de alunos baseada em similaridade de características.
* Identificar comunidades de estudantes com perfis semelhantes.
* Comparar redes utilizando diferentes conjuntos de atributos.
* Investigar fatores associados ao desempenho acadêmico.
* Aplicar métricas de redes para análise estrutural dos grupos.

---

## 📊 Dataset

Foi utilizado o **Student Performance Dataset**, composto por informações acadêmicas, sociais e comportamentais de estudantes do ensino médio de Portugal.

### Principais variáveis analisadas

| Variável  | Descrição                              |
| --------- | -------------------------------------- |
| G1        | Nota do primeiro período               |
| G2        | Nota do segundo período                |
| G3        | Nota final                             |
| studytime | Tempo de estudo                        |
| failures  | Número de reprovações anteriores       |
| absences  | Número de faltas                       |
| goout     | Frequência de saídas com amigos        |
| Walc      | Consumo de álcool nos finais de semana |
| Dalc      | Consumo de álcool durante a semana     |
| higher    | Interesse em cursar ensino superior    |
| paid      | Aulas extras pagas                     |

---

## ⚙️ Metodologia

### 1. Pré-processamento

* Seleção das variáveis relevantes.
* Conversão de atributos categóricos.
* Normalização dos dados utilizando StandardScaler.

### 2. Construção da Rede

Cada aluno foi representado por um nó.

A similaridade entre alunos foi calculada a partir de suas características acadêmicas e comportamentais.

Foram criadas arestas apenas entre alunos suficientemente semelhantes.

### 3. Classificação do Desempenho

A nota final (G3) foi utilizada para categorizar os estudantes em:

* Baixo desempenho
* Médio desempenho
* Alto desempenho

### 4. Análise Estrutural

Foram realizadas:

* Visualização da rede
* Detecção de comunidades
* Identificação de nós isolados
* Análise do grau dos nós
* Comparação entre diferentes configurações da rede

### 5. Análise Estatística

Complementando os grafos, foram utilizadas:

* Médias por categoria
* Tabelas de contingência (crosstab)
* Boxplots
* Matriz de correlação

---

## 📈 Principais Resultados

### Rede com G1 e G2

Ao incluir as notas dos períodos anteriores (G1 e G2), observou-se uma separação mais clara dos grupos de desempenho.

Isso ocorre porque essas variáveis possuem forte correlação com a nota final.

### Rede sem G1 e G2

Ao remover as notas anteriores, a rede tornou-se mais homogênea.

Os grupos de desempenho passaram a apresentar maior mistura, indicando que outras variáveis possuem menor poder discriminatório.

### Reprovações (Failures)

A variável failures apresentou correlação negativa moderada com as notas.

Alunos com maior número de reprovações anteriores tendem a apresentar desempenho inferior.

### Faltas (Absences)

As faltas não apresentaram correlação linear forte com o desempenho, embora tenham contribuído para a formação de alguns perfis específicos na rede.

### Grau dos Nós

Os alunos de alto desempenho apresentaram, em média, maior grau na rede.

Isso sugere que seus perfis acadêmicos são mais semelhantes aos de outros estudantes.

---

## 🔥 Principais Descobertas

* G1 e G2 foram os fatores mais associados ao desempenho final.
* Reprovações anteriores impactam negativamente o desempenho.
* O tempo de estudo apresentou influência positiva, porém fraca.
* O interesse em cursar ensino superior apareceu associado a melhores resultados acadêmicos.
* Variáveis comportamentais como consumo de álcool e saídas com amigos apresentaram correlações entre si.

---

## 🧠 Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* NetworkX
* Scikit-Learn

---


## 🚀 Como Executar

### Instalar dependências

```bash
pip install pandas numpy matplotlib seaborn networkx scikit-learn
```

### Executar o notebook

```bash
jupyter notebook
```

Abrir:

```text
analise_rede_alunos.ipynb
```

---

## 📚 Aprendizados

Durante o desenvolvimento deste projeto foram aplicados conceitos de:

* Ciência de Dados
* Análise Exploratória de Dados
* Teoria dos Grafos
* Detecção de Comunidades
* Similaridade entre observações
* Visualização de Redes Complexas
* Interpretação Estatística

---

