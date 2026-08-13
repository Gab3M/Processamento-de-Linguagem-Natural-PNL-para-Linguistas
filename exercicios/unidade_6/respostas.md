---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 6 - Respostas dos Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Respostas Práticos - Unidade 6: Anotações de Nível de Discurso

1. 

```python
import conllu

text_conllu = (
    "# text = Hello world\n"
    "1\tHello\thello\tINTJ\tUH\t_\t0\troot\t_\t_\n"
    "2\tworld\tworld\tNOUN\tNN\tNumber=Sing\t1\tvocative\t_\t_"
)
sentences = conllu.parse(text_conllu)
```

2. 
```python
sent1 = sentences[0]
# O índice 1 corresponde ao segundo token: 'world'
token_world = sent1[1]
print('Lemma:', token_world['lemma'])
print('UPOS:', token_world['upos'])
```

3. 
```python
words = [token['form'] for token in sent1]
spaces = [True, False] # Considerando sem espaço final na frase
```

4.
```python
import spacy
from spacy.tokens import Doc

nlp = spacy.blank('en')
# Instanciando o Doc manualmente
doc = Doc(nlp.vocab, words=words, spaces=spaces, sent_starts=[True, False])
print('Tokens do Doc gerado:', list(doc))
```

