---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 4 - Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Exercícios — Introdução aos *word embeddings*

Os exercícios abaixo pressupõem que você tenha executado o código da unidade e que as seguintes variáveis estejam disponíveis: `nlp`, `docs`, `df`, `lemma_df`, `unique_lemmas`, `lemma_vectors`, `pairs`, `targets`, `context` e `embedding_model`.

## Parte A — Conceitos

**Exercício 1.** Enuncie a hipótese distribucional em uma frase e explique de que modo a citação de Firth ("*You shall know a word by the company it keeps*") a antecipa.

**Exercício 2.** Explique a diferença entre os eixos **sintagmático** e **paradigmático** de Saussure. Na matriz criada na seção 2.1, o que representam as linhas e o que representam as colunas em relação a esses eixos?

**Exercício 3.** Por que a representação obtida na seção 2.1 é chamada de "saco de palavras" (*bag of words*)? Cite duas limitações dessa representação.

**Exercício 4.** Qual é a diferença entre um vetor **esparso** e um vetor **denso**? Por que os *word embeddings* aprendidos pela camada oculta são densos?

**Exercício 5.** Explique por que a predição da palavra vizinha é descrita como uma **tarefa substituta** (*proxy*) e não como o objetivo real do treinamento.

**Exercício 6.** A camada oculta da rede tem apenas dois neurônios. Explique por que ela é descrita como um "gargalo" e qual o papel desse gargalo no aprendizado das representações.

## Parte B — Programação

**Exercício 7.** Calcule a similaridade de cossenos entre os *Docs* de índices 3 e 4 usando a matriz `df`. O valor obtido é coerente com o conteúdo das duas orações? Justifique.

**Exercício 8.** Acrescente uma sexta oração à lista `examples` — por exemplo, `"Stockholm is the capital of Sweden"` — e refaça o pipeline até a matriz de similaridade de cossenos. Quantas colunas passa a ter o *DataFrame* `df`? Qual *Doc* se torna mais similar ao novo?

**Exercício 9.** Usando a matriz de coocorrência `lemma_df`, calcule a similaridade de cossenos entre os vetores de `'capital'` e `'the'`, e entre `'Helsinki'` e `'ferry'`. Comente os resultados à luz da hipótese distribucional.

**Exercício 10.** Modifique o laço que preenche `lemma_df` para considerar uma janela de **três** palavras de cada lado, em vez de duas. Recalcule a similaridade entre `'Helsinki'` e `'Tallinn'` e compare com o valor obtido na unidade.

**Exercício 11.** Escreva uma função `one_hot(lemma, vocabulary)` que receba um lema e uma lista de lemas e devolva o vetor one-hot correspondente, sem usar o dicionário `lemma_vectors`. A função deve levantar um `ValueError` se o lema não estiver no vocabulário.

**Exercício 12.** Treine novamente a rede neural, desta vez com **quatro** neurônios na camada oculta, mantendo os demais parâmetros. Verifique o formato da matriz de pesos da camada oculta e explique por que já não é possível plotar diretamente o espaço de embeddings em duas dimensões.

**Exercício 13.** A partir da matriz `hidden_layer_weights` obtida na unidade, calcule a similaridade de cossenos entre os embeddings de `'Helsinki'` e `'Tallinn'`. Compare esse valor com o obtido na seção 2.2 a partir da matriz de coocorrência.

## Parte C — Reflexão

**Exercício 14.** O exemplo da unidade usa apenas cinco orações. Liste três consequências concretas dessa escassez de dados para a qualidade dos embeddings aprendidos.

**Exercício 15.** A unidade menciona que abordagens contemporâneas tentam distinguir formas homonímicas como "banco" (instituição) e "banco" (assento). Explique por que o modelo construído nesta unidade é **incapaz** de fazer essa distinção e o que seria necessário para superá-la.
