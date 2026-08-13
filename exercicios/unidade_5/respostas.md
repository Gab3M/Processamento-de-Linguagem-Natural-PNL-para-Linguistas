---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 5 - Respostas dos Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Respostas Práticos - Unidade 5: Embeddings de Palavras no spaCy

1. 
```python
import spacy
# Certifique-se de que o modelo foi baixado previamente: 
#python -m spacy download en_core_web_lg
nlp = spacy.load('en_core_web_lg')
doc = nlp('The cat sat on the mat.')
```

2. 
```python
cat_token = doc[1] # Acessando 'cat'
print('OOV:', cat_token.is_oov)
print('Primeiras 5 dimensões:', cat_token.vector[:5])
```

3. 
```python
doc2 = nlp('The dog sat on the mat.')
dog_token = doc2[1]
print('Similaridade:', cat_token.similarity(dog_token))
```

4. 
```python
frase1 = nlp('I love programming')
frase2 = nlp('Coding is my passion')
print('Similaridade entre frases:', frase1.similarity(frase2))
```

