---
title: "Parte III: Processamento de Linguagem Natural para Linguistas"
subtitle: "Unidade 2 - Respostas dos Exercícios"
author: "CiberExt 26-29 · FEELT38103 · Universidade Federal de Uberlândia"
date: "Agosto de 2026"
lang: "pt-BR"
---

## Gabarito - Módulo 2: Dependências Universais

**Resposta 1:** 
1. Desenvolver um framework comum para descrever a estrutura gramatical de diversos idiomas.
2. Criar corpora anotados (ou *treebanks*) para diversos idiomas aplicando este framework universal.

**Resposta 2:** 
1. **Nominais (*nominals*):** Usados para representar coisas, sendo frequentemente construídos em torno de substantivos (análogos a sintagmas nominais).
2. **Orações (*clauses*):** Usadas para representar eventos, sendo construídas fundamentalmente em torno de verbos. Elas situam-se acima dos nominais hierarquicamente.
3. **Modificadores (*modifiers*):** Dependem de adjetivos e advérbios e servem para expandir, refinar e detalhar o significado tanto de nominais quanto de orações.

**Resposta 3:** 
A etiqueta `root` identifica a **raiz** ou a cabeça central da oração (geralmente o verbo principal). No framework UD, as dependências são desenhadas de cabeça para cabeça; portanto, os arcos sintáticos partem da raiz (o verbo) em direção às palavras que atuam como as cabeças dos nominais dependentes (como o pronome sujeito ou o substantivo objeto direto).

**Resposta 4:** 
O atributo `token.subtree` retorna um gerador que contém todos os dependentes diretos e indiretos (filhos, netos, bisnetos, etc.) **incluindo o próprio *Token* original**. O atributo `token.children`, por outro lado, retorna apenas os dependentes imediatos (filhos diretos de primeiro nível) e **não inclui o *Token* original** na sua saída.

**Resposta 5:** 
Essas métricas penalizam desproporcionalmente idiomas morfologicamente ricos. Em inglês, as sentenças são mais longas devido ao alto uso de palavras de função independentes (preposições, auxiliares); logo, errar uma palavra causa um pequeno impacto percentual. Em finlandês, onde essas funções são acopladas nas palavras originais (formando sentenças mais curtas), um único erro sintático representa uma porcentagem de perda muito maior na métrica final. 
Métricas alternativas sugeridas incluem a **CLAS** (*content-labeled attachment score*), que ignora palavras de função na contagem, a **MLAS** (com foco na morfologia) e a **BLEX** (com foco no lema).

---