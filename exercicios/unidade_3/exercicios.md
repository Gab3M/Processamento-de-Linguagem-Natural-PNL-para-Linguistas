---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 3 - Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

# Exercícios — Encontrando padrões linguísticos com o spaCy

Os exercícios abaixo pressupõem que você tenha executado o código da unidade e que as seguintes variáveis estejam disponíveis: `nlp`, `doc`, `matcher`, `morph_matcher` e `dep_matcher`.

Para os exercícios de programação, use um modelo pequeno para o inglês (`en_core_web_sm`) e o arquivo `data/occupy.txt` utilizado na unidade.

## Parte A — Conceitos

**Exercício 1.** Explique, com suas próprias palavras, a diferença entre as classes *Matcher*, *DependencyMatcher* e *PhraseMatcher* do spaCy. Dê um exemplo de tarefa linguística adequada a cada uma.

**Exercício 2.** No formato de padrões do spaCy, qual é o papel da chave `OP`? Descreva o efeito de cada um dos quatro operadores (`!`, `?`, `+`, `*`) e dê um exemplo de padrão em que o operador `?` seria preferível ao `+`.

**Exercício 3.** Qual a diferença entre as chaves `POS` e `TAG` em uma regra de padrão? Por que a etiqueta `NNP` não aparece como valor de `POS`?

**Exercício 4.** Explique o funcionamento do atributo `IS_SUPERSET` aplicado à chave `MORPH`. Por que ele é necessário quando queremos casar apenas *alguns* traços morfológicos?

**Exercício 5.** No *DependencyMatcher*, explique a diferença entre as chaves `LEFT_ID` e `RIGHT_ID`. Por que o primeiro dicionário de um padrão não possui `LEFT_ID`?

**Exercício 6.** Por que o *DependencyMatcher* devolve tuplas de índices em vez de objetos *Span*, como faz o *Matcher*?

## Parte B — Programação

**Exercício 7.** Crie um *Matcher* que encontre sequências de um adjetivo (`ADJ`) seguido de um substantivo (`NOUN`) no objeto `doc`. Nomeie o padrão como `adj+noun` e imprima as 20 primeiras correspondências.

**Exercício 8.** Modifique o padrão do exercício anterior para permitir **um ou mais** adjetivos antes do substantivo. Compare a quantidade de correspondências obtidas com e sem o argumento `greedy='LONGEST'` e explique a diferença.

**Exercício 9.** Escreva um padrão que case substantivos no plural, usando a chave `MORPH` com `IS_SUPERSET` e o traço `Number=Plur`. Imprima as 15 primeiras correspondências junto com os traços morfológicos de cada *Token*.

**Exercício 10.** Usando o *DependencyMatcher*, escreva um padrão que encontre verbos (`VERB`) e seus objetos diretos (`dobj`), sem incluir o sujeito. Nomeie o padrão como `verb_dobj` e imprima as 20 primeiras correspondências no formato `verbo ... objeto`.

**Exercício 11.** Estenda o padrão do exercício anterior acrescentando um terceiro elo à corrente: o **determinante** (`det`) do objeto direto. Note que esse novo elo deve partir do padrão `d_object`, e não da âncora `verb`. Imprima as correspondências no formato `verbo ... determinante objeto`.

**Exercício 12.** Escreva um laço que produza linhas de concordância para as correspondências do exercício 7, exibindo 5 *Tokens* antes e 5 *Tokens* depois de cada correspondência, com o trecho casado destacado em azul usando a classe `Printer` da wasabi.

## Parte C — Reflexão

**Exercício 13.** As linhas de concordância da unidade às vezes "pulam" uma ou duas linhas na saída. Explique a causa e proponha uma solução em Python que evite esse comportamento.

**Exercício 14.** Suponha que você queira estudar a construção "verbo + preposição + sintagma nominal" (por exemplo, *depend on the government*) em um corpus. Descreva qual *Matcher* você usaria e esboce a regra de padrão correspondente, justificando suas escolhas.
