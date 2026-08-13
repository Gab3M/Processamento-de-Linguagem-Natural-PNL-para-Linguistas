---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 5 - Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Exercícios Práticos - Unidade 5: Embeddings de Palavras no spaCy

1. Carregue o modelo de linguagem `en_core_web_lg` do spaCy e crie um objeto `Doc` para a frase 'The cat sat on the mat.'.

2. Verifique se o token 'cat' está presente no vocabulário (usando a propriedade `is_oov`) e imprima as 5 primeiras dimensões do seu vetor de embeddings.

3. Calcule e imprima a similaridade de cosseno (cosine similarity) entre os tokens 'cat' e 'dog' (lembre-se de processar 'dog' com o nlp antes).

4. Calcule a similaridade entre duas frases completas (objetos `Doc`): 'I love programming' e 'Coding is my passion'.

