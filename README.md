# Atividade 1 – Curadoria de Datasets e Inferência com LLMs

## Equipe 4 – Domínio Jurídico

**Discente:** José Bruno Barros dos Santos

---

## 1. Visão Geral

Este repositório apresenta a execução completa da Atividade Avaliativa 1 da disciplina *Tópicos Avançados em Engenharia de Software e Sistemas de Informação*, com foco na curadoria de datasets jurídicos e na avaliação comparativa de modelos de linguagem (LLMs).

A atividade foi desenvolvida a partir de datasets do exame da OAB, envolvendo tanto questões discursivas (abertas) quanto questões de múltipla escolha, permitindo analisar o desempenho dos modelos em diferentes tipos de tarefa.

---

## 2. Objetivos

* Realizar a curadoria de questões jurídicas
* Aplicar inferência com modelos de linguagem (LLMs)
* Avaliar qualitativamente respostas discursivas
* Avaliar quantitativamente questões objetivas
* Comparar o desempenho entre diferentes modelos

---

## 3. Datasets Utilizados

### Dataset J1 – Questões Abertas

* Fonte: OAB Bench (maritaca-ai)
* Total: 210 questões
* Subconjunto utilizado: **119 a 130**

### Dataset J2 – Múltipla Escolha

* Fonte: eduagarcia/oab_exams
* Subconjunto utilizado: **1231 a 1353**

---

## 4. Metodologia

A metodologia foi dividida em três etapas principais:

---

### 4.1 Curadoria dos Dados

Cada questão foi analisada e classificada com base nos seguintes critérios:

* **Nível de dificuldade**
* **Área jurídica**
* **Subárea temática**
* **Referência legal principal e secundária**
* **Observações analíticas**

A classificação seguiu uma abordagem interpretativa e técnica, com base na legislação brasileira.

---

### 4.2 Inferência com Modelos de Linguagem

Foram utilizados três modelos:

* ChatGPT
* Gemini
* Grok

Para cada questão discursiva, foi aplicado o seguinte padrão de prompt:

```
Você é um candidato da segunda fase da OAB.
Responda à questão jurídica abaixo de forma discursiva, objetiva, fundamentada e tecnicamente correta.
Instruções:
1. Utilize linguagem jurídica clara.
2. Apresente a tese jurídica principal.
3. Fundamente com base legal pertinente.
4. Quando cabível, articule princípios, normas e interpretação.
5. Evite prolixidade.
6. Não invente fatos que não constam no enunciado.
7. Estruture a resposta em parágrafos curtos.
[QUESTÃO]
[ITENS]
```

As respostas foram coletadas e armazenadas para posterior análise.

---

### 4.3 Avaliação das Respostas

As respostas foram avaliadas com base nas seguintes métricas qualitativas:

* Clareza
* Precisão jurídica
* Fundamentação legal
* Coesão argumentativa
* Completude
* Adequação ao caso
* Segurança técnica

Cada critério foi pontuado de 1 a 5, permitindo gerar uma pontuação total por resposta.

---

### 4.4 Avaliação das Questões de Múltipla Escolha

Para as questões objetivas, foi realizada análise quantitativa baseada em:

* Comparação com o gabarito oficial
* Cálculo de acurácia (%) por modelo

---

## 5. Pipeline de Implementação

A implementação foi realizada em Python, utilizando:

* `pandas` → manipulação de dados
* `requests` → consumo de dataset
* `json` → parsing
* `openpyxl` → exportação

### Etapas:

1. Carregamento do dataset
2. Filtragem do subconjunto
3. Estruturação dos DataFrames:

   * `df_respostas`
   * `df_avaliacao`
   * `df_curadoria`
4. Inserção das respostas dos modelos
5. Aplicação das métricas
6. Consolidação dos resultados
7. Exportação para Excel

---

## 6. Resultados

###  Questões Discursivas

| Modelo  | Desempenho |
| ------- | ---------- |
| Grok    | 🥇 Melhor  |
| Gemini  | 🥈         |
| ChatGPT | 🥉         |

O modelo **Grok** apresentou maior precisão jurídica e melhor adequação normativa.

---

###  Múltipla Escolha

| Modelo  | Acurácia  |
| ------- | --------- |
| Gemini  | 🥇 95,93% |
| Grok    | 🥈        |
| ChatGPT | 🥉        |

O modelo **Gemini** demonstrou maior eficiência em tarefas objetivas.

---

## 7. Análise Crítica

Os resultados evidenciam que:

* Modelos apresentam melhor desempenho em tarefas objetivas
* A interpretação jurídica ainda representa um desafio relevante
* A atualização legislativa impacta diretamente a qualidade das respostas

Além disso, observa-se que diferentes modelos possuem especializações implícitas, sendo mais adequados a determinados tipos de tarefa.

---

## 8. Conclusão

Os modelos de linguagem demonstram alto potencial de aplicação no domínio jurídico, especialmente como ferramentas de apoio.

Entretanto, ainda apresentam limitações quanto à precisão técnica e confiabilidade, sendo indispensável a validação humana, principalmente em contextos profissionais.

---

## 9. Estrutura do Repositório

```
/notebooks
/resultados
/pdf
README.md
```

---

## 10. Artefatos Gerados

* Planilha consolidada de resultados
* Avaliação dos modelos
* Curadoria das questões
* Relatório em PDF
* Notebook com execução completa

---

## 11. Vídeo Demonstrativo

 (Inserir link aqui)

---

## 12. Contribuição Individual

José Bruno Barros dos Santos foi responsável por:

* Curadoria das questões 119 a 130
* Implementação do pipeline em Python
* Execução das inferências
* Avaliação qualitativa
* Processamento das questões de múltipla escolha
* Consolidação e análise dos resultados

---

## 13. Considerações Finais

Este projeto demonstra a aplicação prática de LLMs no domínio jurídico, contribuindo para a compreensão dos limites e potencialidades dessas tecnologias no contexto acadêmico e profissional.

---
