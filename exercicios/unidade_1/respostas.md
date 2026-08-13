---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 1 - Respostas dos Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

## Gabarito - Módulo 1: Processando Diversos Idiomas

**Resposta 1:** 
Os dois principais desafios estruturais são:
1. **Morfologia complexa:** Idiomas aglutinativos (como finlandês e turco) podem combinar a raiz, o tempo verbal, marcadores de caso e pronomes em uma única palavra, diferentemente do inglês.
2. **Ordem das palavras (Sintaxe):** Enquanto o inglês segue uma ordem estrita Sujeito-Verbo-Objeto (SVO), muitos outros idiomas possuem ordens flexíveis ou adotam estruturas diferentes, como Sujeito-Objeto-Verbo (SOV), comum no japonês.

**Resposta 2:**
```python
import stanza

# Baixa o modelo de linguagem para o finlandês
stanza.download(lang='fi')

# Inicializa o pipeline apenas com o tokenizador 
# e o etiquetador de classes gramaticais
nlp_fi = stanza.Pipeline(lang='fi', processors='tokenize, pos')
```

**Resposta 3:** 
Deve-se utilizar o método `to_dict()`. Este método converte o objeto *Sentence* em uma lista de dicionários onde cada dicionário representa um único objeto *Token*, contendo as anotações linguísticas na forma de pares chave-valor (ex: 'id', 'text', 'lemma', 'upos').

**Resposta 4:** 
A maneira mais eficiente é não passar string por string, mas coletá-las em uma lista e pré-empacotá-las em objetos *Document*. O passo a passo seria:
1. Reunir os textos como strings em uma lista padrão (ex: `str_docs`).
2. Utilizar uma compreensão de lista para criar uma nova lista instanciando documentos vazios preenchidos apenas com o texto: `docs_in = [stanza.Document([], text=doc) for doc in str_docs]`.
3. Passar a lista completa `docs_in` diretamente para o objeto do modelo de linguagem (pipeline) de uma só vez para realizar a anotação.

**Resposta 5:** 
A limitação é que **o idioma em questão deve ser suportado nativamente tanto pelo Stanza quanto pelo spaCy**. Se tentarmos processar o idioma Wolof, por exemplo, não será possível usar o `spacy-stanza`, pois o spaCy não possui suporte a esse idioma em seu framework de base.

---
