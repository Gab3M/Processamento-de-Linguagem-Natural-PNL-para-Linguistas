---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 6 - Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Exercícios Práticos - Unidade 6: Anotações de Nível de Discurso

1. Importe a biblioteca `conllu` e faça o parse da seguinte string CoNLL-U para criar uma lista de sentenças:
```python
text_conllu = (
    "# text = Hello world\n"
    "1\tHello\thello\tINTJ\tUH\t_\t0\troot\t_\t_\n"
    "2\tworld\tworld\tNOUN\tNN\tNumber=Sing\t1\tvocative\t_\t_"
)
```

2. Acesse a primeira sentença gerada (do exercício anterior) e imprima o `lemma` e a `upos` (part-of-speech tag universal) da palavra 'world'.

3. A partir dos tokens extraídos da anotação, crie uma lista `words` iterando para pegar a forma textual (`form`) e defina manualmente uma lista `spaces = [True, False]`.

4. Utilize as listas geradas (e `sent_starts=[True, False]`) para instanciar um objeto `Doc` manualmente (importando `Doc` de `spacy.tokens`) em um modelo em branco (`spacy.blank('en')`).

