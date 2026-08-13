# Processamento de Linguagem Natural (PNL) para Linguistas 📚🐍

Bem-vindo ao repositório do curso de Processamento de Linguagem Natural (PNL)! Este projeto reúne materiais didáticos, anotações e exemplos práticos traduzidos e adaptados para o português, com foco em ferramentas modernas de PNL no ecossistema Python.

Este material é uma adaptação do curso open-source [Applied Language Technology](https://applied-language-technology.mooc.fi/), originalmente desenvolvido por Tuomo Hiippala, com objetivo de tornar o conteúdo acessível a estudantes e pesquisadores de linguística, letras e áreas afins.

## 🎯 Público-alvo e Objetivos

* Estudantes de Linguística, Letras e áreas correlatas.
* Pessoas interessadas em aprender sobre PNL aplicada à análise linguística.
* Usuários que desejam explorar ferramentas de processamento textual com foco em diversidade linguística.

### Objetivos do Projeto

* Disponibilizar conteúdo acadêmico e prático de alta qualidade sobre PNL em português.
* Ensinar o processamento de textos em diversos idiomas usando bibliotecas modernas.
* Demonstrar a aplicação prática de frameworks de anotação, como as **Dependências Universais (UD)**.
* Conectar teoria linguística e prática computacional de forma acessível.

## 🛠️ Tecnologias Utilizadas

As seguintes bibliotecas e ferramentas formam a base deste curso:

* **[Python 3](https://www.python.org/):** A linguagem base para todos os scripts e automações.
* **[spaCy](https://spacy.io/):** Biblioteca de nível industrial para processamento de linguagem natural.
* **[Stanza](https://stanfordnlp.github.io/stanza/):** Pacote Python oficial do Stanford NLP Group para análise em múltiplos idiomas.
* **[spacy-stanza](https://spacy.io/universe/project/spacy-stanza):** Wrapper que permite usar os modelos do Stanza com a sintaxe e o ecossistema do spaCy.
* **[Jupyter Notebooks](https://jupyter.org/) / Markdown:** Para documentação interativa e visualização de dados.

## 🚀 Como Começar

Para rodar os códigos e explorar os materiais deste repositório, você precisará configurar o seu ambiente Python. Recomenda-se o uso de um ambiente virtual (como `venv` ou `conda`).

### Requisitos

* Python 3.9 ou superior.
* Ambiente virtual recomendado para isolar dependências.
* `pip` atualizado.
* Acesso à internet para baixar modelos e bibliotecas.

**1. Clone o repositório:**
```bash
git clone https://github.com/Gab3M/Processamento-de-Linguagem-Natural-PNL-para-Linguistas
cd Processamento-de-Linguagem-Natural-PNL-para-Linguistas
```

**2. Crie e ative um ambiente virtual:**
```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# .venv\Scripts\activate   # Windows
```

**3. Instale as dependências:**
```bash
pip install --upgrade pip
pip install spacy stanza spacy-stanza jupyter
```

**4. Faça o download dos modelos de linguagem necessários:**
(Exemplo para baixar o modelo em inglês no Stanza)
```python
import stanza
stanza.download('en')
```

### Como usar este material

* Leia os materiais teóricos em ordem, começando pela unidade 1.
* Acesse os exercícios e tente resolvê-los antes de consultar as respostas.
* Use os arquivos em Markdown e HTML como apoio para a leitura e revisão.
* Execute os exemplos em Python para experimentar os conceitos em prática.
* Caso algum modelo ou biblioteca precise de download inicial, aguarde a instalação e repita a execução.

#### Visualizar o site (index.html)

Se quiser visualizar a versão estática do material no navegador, abra o arquivo `index.html` diretamente ou sirva a pasta localmente. Exemplo (recomendado):

```bash
# a partir da raiz do repositório ou dentro
python3 -m http.server 8000

# então abra no navegador:
http://localhost:8000/
```

Abrir via servidor local evita problemas de carregamento de recursos e permite navegar pelas páginas relativas corretamente.


## 📚 Roteiro de Aprendizado

A sequência recomendada de estudo é a seguinte:

| Módulo | Conteúdo principal |
| --- | --- |
| `unidade_1` | Processamento de diversos idiomas e introdução às etapas básicas de PNL. |
| `unidade_2` | Dependências universais e análise sintática em perspectiva multilíngue. |
| `unidade_3` | Padrões linguísticos e estruturas recorrentes em textos. |
| `unidade_4` | Introdução aos word embeddings e representações distribuídas de palavras. |
| `unidade_5` | Word embeddings no spaCy e aplicação prática em modelos de linguagem. |
| `unidade_6` | Anotações de nível de discurso e organização textual. |

## 📁 Estrutura do Repositório

* `/unidade_1`: Processando Diversos Idiomas.
* `/unidade_2`: Dependências Universais.
* `/unidade_3`: Padrões Linguisticos.
* `/unidade_4`: Introdução aos Word Embeddings.
* `/unidade_5`: Word Embeddings no spaCy.
* `/unidade_6`: Anotações de nível de discurso.
* `/resources`: Capturas de tela e gráficos de árvores de dependência.
* `/exercicios`: Exercicios de fixação e gabaritos para cada unidade.

## 📝 Observações Importantes

* A primeira execução de alguns exemplos pode levar mais tempo, pois os modelos precisam ser baixados.
* Algumas bibliotecas podem requerer versões específicas de dependências em ambiente local.
* O uso de um ambiente virtual é recomendado para evitar conflitos entre projetos Python.
* Se houver erros de importação ou modelos ausentes, revise a instalação e confirme se os pacotes foram corretamente baixados.

## 🛠️ Troubleshooting

Alguns problemas comuns durante a execução do material incluem:

* `ModuleNotFoundError`: verifique se o ambiente virtual está ativado e se as dependências foram instaladas corretamente.
* Erros ao baixar modelos do `stanza`: confirme sua conexão com a internet e tente novamente.
* Compatibilidade de versões: confira se a versão do Python e dos pacotes estão em conformidade com o curso.
* Erros em notebooks ou scripts: recomende-se reiniciar o kernel e executar as células em ordem.

## 🤝 Contribuições

Contribuições, correções e sugestões são bem-vindas. Se você encontrar erros, tiver melhorias para o material ou quiser adaptar o conteúdo para outra audiência, sinta-se à vontade para abrir uma issue, propor uma atualização ou entrar em contato com os responsáveis pelo repositório.

Este projeto também pode ser expandido com novos exemplos, exercícios complementares, materiais em outros idiomas e melhorias de documentação.

## ⚖️ Licença e Créditos

Este repositório é uma tradução e adaptação independente. O material original foi criado por **Tuomo Hiippala** em colaboração com a plataforma MOOC.fi (Universidade de Helsinque).

Todo o conteúdo deste repositório está licenciado sob a licença **[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)**. 

Isso significa que você é livre para compartilhar e adaptar este material, desde que dê os devidos créditos aos autores originais e não o utilize para fins comerciais. Veja o arquivo `LICENSE` para mais detalhes.
