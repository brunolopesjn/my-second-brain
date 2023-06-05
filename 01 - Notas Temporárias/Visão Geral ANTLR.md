---
created-at: 2023-06-04 21:33
updated-at: 04/06/2023 21:33:23
---

#antlr4 

# Capítulo 2 - Visão Geral

- Para implementar uma linguagem, nós temos que construir uma aplicação que seja capaz de ler sentenças e reaja adequadamente as frases e os símbolos de entrada que descobre.
- Uma **linguagem** é um conjunto de  de **sentenças válidas**, uma sentença é formada de **frases** e frases são formadas de subfrases e símbolos de vocabulário.
- De forma ampla:
	- Se uma aplicação computa ou executa sentenças, nós chamamos essa aplicação de **interpretador** (e.g. calculadora e Python);
	- Se uma aplicação converte sentenças de uma linguagem para outra, nó chamamos essa aplicação de **tradutor** (e.g. Java e C#).
- Para reagir de forma apropriada, o interpretador precisa reconhecer todas as sentenças válidas, frases e subfrases de uma linguagem em particular.
- Reconhecer uma frase significa que podemos identificar os diversos componentes e podemos diferenciar eles de outras frases.
- Programas que reconhecem linguagens são chamados de **analisadores sintáticos** ou simplesmente de **analisadores** (_parser_).
- Quando nos referimos a sintaxe, estamos falando das regras que definem os componentes de uma linguagem e iremos construir **gramáticas ANTLR** para especificar uma sintaxe de uma linguagem.
- A ferramenta ANTLR realiza a tradução de uma gramática para um _parser_, que são similares aos escritos  por uma pessoa desenvolvedora experiente.
- As próprias gramáticas seguem a sintaxe de uma linguagem otimizada para especificar outras linguagens, em outras palavras, o _ANTLR_ é uma meta-linguagem.
- O processo de análise é muito mais simples se quebrarmos em duas tarefas ou estágios semelhantes mas distintos:
	- O processo de agrupar caracteres em palavras ou símbolos (**tokens**) é chamado de **análise léxica** ou simplesmente de **tokenização**.
		- Nós chamamos o programa que realiza a tokenização de uma entrada de **lexer**
		- Um _lexer_ pode agrupar símbolos relacionados em **classes de símbolos** ou **tipos de símbolos** como, por exemplo, INT (inteiro), ID (identificadores), FLOAT (números de ponto flutuante), etc.
		- Um símbolo (_token_) é composto de, pelo menos, duas partes: o tipo de símbolo (identificando a estrutura léxica) e o texto correspondente do simbolo pelo _lexer_.
	- O analisador que utiliza dos simbolos reconhecidos pelo _lexer_ para reconhecer a estrutura de uma frase.
		- Por padrão os analisadores gerados pelo _ANTLR_ controem uma estrutura de dados chamada de **árvore de análise** (_parse tree_) ou **árvore de sintaxe** (_syntax tree_) que tem como objetivo armazenar como o analisador reconheceu a estrutura da sentença de entrada e suas respectivas frases.
- 

# Referências
- [[The Definitive ANTLR4 Reference]]