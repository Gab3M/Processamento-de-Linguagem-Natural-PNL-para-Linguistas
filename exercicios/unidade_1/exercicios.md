---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 1 - Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Exercícios Práticos: Processamento de Linguagem Natural para Linguistas

Este documento contém exercícios práticos baseados na unidade "Processando Diversos Idiomas".

## Módulo 1: Processando Diversos Idiomas

**Exercício 1:** Historicamente, as ferramentas de Processamento de Linguagem Natural (PNL) foram desenvolvidas com forte foco no idioma inglês. Explique dois desafios estruturais significativos encontrados ao tentar aplicar essas mesmas ferramentas convencionais para outros idiomas, como o finlandês, turco ou o japonês.

**Exercício 2:** Utilizando a biblioteca Stanza, escreva o código Python necessário para fazer o download do modelo de linguagem para o idioma finlandês (código de idioma `'fi'`). Em seguida, inicialize um pipeline (*Pipeline*) que inclua exclusivamente os processadores de tokenização e etiquetagem de classes gramaticais (POS).

**Exercício 3:** Após processar um texto no Stanza, a saída gerada para uma sentença não é uma lista comum do Python, mas um objeto *Sentence*. Qual método nativo da biblioteca você pode utilizar para converter as anotações linguísticas desse objeto em uma lista de dicionários Python, facilitando a interação com as anaves/valores?

**Exercício 4:** Qual é a maneira mais eficiente, em termos de custo computacional e estruturação de código, para processar múltiplos textos (documentos) de uma só vez utilizando o Stanza? Descreva os passos técnicos utilizando a sintaxe de compreensão de listas (*list comprehension*).

**Exercício 5:** A biblioteca `spacy-stanza` é uma excelente ferramenta para integrar os modelos pesados do Stanza dentro do ecossistema familiar do spaCy. Apesar dessa vantagem, o texto menciona uma "grande limitação" para o seu uso. Qual é essa limitação? Dê um exemplo de idioma que ilustra esse problema.

---