# O que é um Computador?

Um computador é um **sistema computacional** composto por um conjunto de dispositivos físicos (**_hardware_**) e de programas (**_software_**).

## Hardware
O _hardware_ são circuitos eletrônicos que estão interligados entre si, formando a parte física do computador. Esses circuitos são formados por processadores, memórias, registradores, barramentos, monitores de vídeo, impressoras, mouse, discos de armazenamentos, além de outros dispositivos físicos.

Todos com componentes de _hardware_ de um sistema computacional podem ser agrupados em três categorias chamadas de **unidades funcionais**:
	- Processador ou Unidade Central de Processamento ( do inglês **_Computer Processing Unit_** - **CPU**);
	- Memória principal;
	- Dispositivos de Entrada e Saída;

### Processador
A principal função do processador é controlar e executar as instruções presentes na memória principal utilizando operações básicas como, por exemplo, somar, subtrair, comparar e movimentar dados. Um processador é composto por três partes: **Unidade de Controle**; **Unidade Lógica** e **Aritmética e Registradores**.

A **Unidade de Controle** (UC) é responsável por gerenciar as atividades de todos os componentes do computador como, por exemplo, a gravação de dados em discos ou a busca de instruções na memória principal.

Já a **Unidade Lógica e Aritmética** (ULA) é responsável pela realização de operações lógicas (testes e comparações) e aritméticas (somas e subtrações).

Por sua vez, os **registradores** são dispositivos que possuem a função de armazenar dados temporariamente no processador. O conjunto de registradores funcionam como uma memória interna do processador de alta velocidade mas com capacidade de armazenamento reduzida e custo de fabricação maior do que a memória principal.

Podemos classificar os registradores em dois tipos:
- **registradores de uso geral**: os quais podem ser manipulados diretamente por instruções;
- **registradores de uso específico**: responsáveis por armazenar informações de controle do processamento e do sistema operacional.

Entre os registradores de uso específico, merecem destaque:
- O **contador de instruções** (CI) armazena o endereço de memória da próxima instrução que o processador deve buscar e executar. Toda vez que o processador busca por uma nova instrução, este registrador é atualizado com o endereço de memória da próxima instrução a ser executada.
- O **apontador de pilha** (AP) armazena  o endereço de memória do topo da pilha, que é a estrutura de dados onde é mantido todas as informações sobre o programa que está sendo executado.
- O **registrador  de instruções** (RI) é responsável por armazenar a instrução que será decodificada e executada pelo processador.
- O **registrador de estado** é responsável por armazenar informações sobre a execução das instruções como, por exemplo, a ocorrência de **_overflow_**. A maioria das instruções, quando executadas, modifica o registrador de estado conforme o resultado da operação.

A forma como o processador executa os programas armazenados na memória principal é chamado de **ciclo de busca de instrução** e segue as etapas descritas a seguir:
1. O processador busca na memória principal a instrução armazenada no endereço de memória  indicado pelo registrador **contador de instruções** e armazena a instrução no **registrador de instruções**;
2. O processador incrementa o **contador de instruções** de modo que contenha o endereço de memória da próxima instrução;
3. O processador decodifica a instrução armazenada no **registrador de instruções**;
4. O processador busca os operandos na memória, se houver;
5. O processador executa a instrução decodificada;

Se houver mais instruções a serem executadas, o processo se repete.

### Memória Principal
A memória principal é o local onde são armazenados as instruções dos programas e os dados. A memória é composta por várias unidades chamadas de células, sendo cada célula composta por um determinado número de **bits**.

O **bit** é a unidade de medida básica da memória, podendo assumir valor lógico **zero** ou **um**. Atualmente a grande maioria dos computadores utilizam o **byte** (agrupamento de 8 bits) como tamanho de célula.

Logo, a memória é constituída por um conjunto de células, onde cada uma delas possui um determinado número de bits. Todas as células da memória principal são numeradas iniciando-se do **zero**, ou seja, a primeira célula possui endereço zero, a segunda endereço um e assim sucessivamente.

Esses números recebem o nome de **endereço** e quando for necessário realizar uma operação de leitura em uma célula, seu endereço (número) deve ser especificado.

A memória principal pode ser classificada de acordo com a sua volatilidade, que é a capacidade da memória de preservar seu conteúdo mesmo sem uma fonte de alimentação ativa. Em outras palavras, temos:
- Memórias do tipo **Random Access Memory** (RAM) que são do tipo voláteis, ou seja, que **não preservam** o conteúdo das células mesmo sem uma fonte de alimentação ativa;
- Memórias do tipo **Read-Only Memory** (ROM) e **Erasable Programmable ROM** (EPROM) que são do tipo não voláteis, ou seja, que **preservam** o conteúdo das células mesmo sem uma fonte de alimentação ativa.

### Dispositivos de Entrada e Saída

**Dispositivos de Entrada e Saída** (ES) ou do inglês **Input Output Devices** (IO) são utilizados para permitir a comunicação entre o sistema computacional com o mundo externo. 

Podemos dividir os dispositivos de entrada e saída em duas categorias: 
- _Os que servem como memória secundária_ como, por exemplo, discos de armazenamento sólido, discos elétrico magnéticos e fitas magnéticas caracterizam-se por ter a capacidade de armazenamento bastante superior ao da memória principal e custo relativamente baixo, porém o tempo de acesso à memória secundária é bem superior ao da memória principal.
- _Os que servem como interface humano-máquina_ como, por exemplo, monitores de vídeo, teclado, _mouse_, dispositivos de áudio, impressoras e etc, tem como finalidade permitir que pessoas menos especializadas utilizem computadores de maneira intuitiva.

## Software

Para que o hardware tenha utilidade prática, deve existir um **conjunto de programas** que servem como interface entre as necessidades das pessoas que utilizam um computador e as capacidades do hardware em uso.

Um **programa** é composto por uma sequência de instruções, que podem ser em linguagem natural ou codificada (linguagem de programação), que é interpretada e executada por um processador ou por uma máquina virtual.

Já um **software** é composto por diversas funções, bibliotecas e módulos que geram um programa executável no fim do processo de desenvolvimento e que, quando executado, recebe algum tipo de entrada de dados _(input)_, processa as informações segundo uma série de algoritmos ou sequências de instruções lógicas e retorna uma saída _(output)_, como resultado deste processamento.

O termo **software** foi criado na década de 1940, e é um trocadilho com o termo **hardware** que, em inglês, significa **ferramenta física**. _Software_ seria tudo o que faz o computador funcionar através de instruções, executando-se a parte física dele.

Apesar das diferenças conceituais dos termos **software** e **programa**, sempre trataremos ambos os termos como sinônimos.

### Tradutor

Nos primeiros sistemas computacionais, o ato de programar um computador era bastante complicado, já que a pessoa programadora deveria possuir conhecimento da arquitetura do sistema computacional e programa-lo através de painéis utilizando fios. Esses programas eram desenvolvidos em linguagem de máquina e carregados diretamente na memória principal para execução.

Com o surgimento das primeiras **linguagens de montagem** ou **_assembly_** e das **linguagens de alto nível**, o programador deixou de se preocupar com muitos aspectos pertinentes ao hardware como, por exemplo, em qual região de memória o programa deveria ser carregado ou quais endereços de memória seriam reservados para as variáveis.

Apesar das inúmeras vantagens das linguagens de montagem e de alto nível, os programas escritos nessas linguagens , chamados de **programa-fonte**, não estão prontos para serem diretamente executados pelo processador.

Para isso, eles têm de passar por uma etapa de conversão, onde toda representação simbólica das instruções é traduzida para código de máquina. Essa conversão é realizada por um utilitário de software chamado **tradutor**.

O módulo gerado pelo tradutor é denominado **módulo-objeto**, que, apesar de estar em código de máquina, na maioria das vezes não pode ser executado ainda. Isso ocorre em uma função de um programa poder realizar chamadas a sub-rotinas externas e, nesse caso, o tradutor não tem como associar o programa principal às sub-rotinas chamadas.

Dependendo do tipo de programa-fonte, exitem dois tipos de tradutores que geram código aberto:
- O **montador** (**_assembler_**) é o software utilitário responsável por traduzir um programa fonte em linguagem de montagem em um programa-objeto não executável. A linguagem de montagem é particular de cada processador, assim como a linguagem de máquina, o que não permite que programas _assembly_ serem portados entre máquinas diferentes.
- O **compilador** é o utilitário responsável por gerar, a partir de um programa escrito em uma linguagem de alto nível, um programa de linguagem de máquina não executável. As linguagens  de alto nível, como C/C++, Rust e Go, não tem nenhuma relação direta com a máquina, ficando essas preocupação exclusivamente com o compilador.

#### Linker

O **linker** ou **editor de ligação** é o utilitário de software responsável por gerar, a partir de um ou mais módulos objeto, um único programa executável. Suas funções básicas são resolver todas as referências simbólicas existentes entre os módulos e reservar memória para execução do programa.

Para resolver todas as referências a símbolos, o **linker** pode pesquisar em bibliotecas do sistema ou da própria pessoa desenvolvedora. Bibliotecas são arquivos que contêm diversos módulos-objetos e definições de símbolos.

#### Loader

O **_loader_** ou **carregador** é o utilitário responsável por carregar na memória principal um programa para ser executado. O procedimento de carga varia com o código gerado pelo **linker** e, em função deste, o **loader** é classificado como do tipo **absoluto** ou **relocável**.

Se o código fonte dor do tipo absoluto, o _loader_ só necessita conhecer o endereço de memória inicial e o tamanho do módulo para realizar o carregamento. Então, o _loader_ transfere o programa da memória secundária para a memória principal e inicia a sua execução (**_loader_ absoluto**).

No caso do código relocável, o programa pode ser carregado em qualquer posição de memória , e o _loader_ é responsável pela realozação no momento do carregamento (**_loader_ relocável**).

### Interpretador

A partir da execução de um programa-fonte escrito em linguagem de alto nível, o interpretador, durante a execução do programa, traduz cada instrução e a executa imediatamente. Algumas linguagens tipicamente interpretadas são Python, JavaScript, PHP e Ruby.

A maior desvantagem no uso de interpretadores é o tempo gasto na tradução das instruções de um programa toda vez que este for executado, já que não existe a geração de um código executável.

Entretanto, existe a vantagem em implementar tipos de dados dinâmicos, ou seja, que podem mudar de tipo durante a execução do programa, aumentando, assim sua flexibilidade.

#### Depurador

O desenvolvimento de programas está sujeito a erros de lógica, independente das metodologias de desenvolvimento utilizadas pela pessoa desenvolvedora.

A **depuração** é um dos estágios desse desenvolvimento, e a utilização de ferramentas adequadas é essencial para acelerar o processo de correção de erros dos programas.

O depurador (**debbuger**) é o utilitário que permite a pessoa desenvolvedora acompanhar toda a execução de um programa a fim de detectar erros na sua lógica.

Esse utilitário oferece recursos como:
- Acompanhar a execução de um programa instrução por instrução;
- Possibilitar a alteração e a visualização do conteúdo de variáveis;
- Implementar pontos de parada dentro do programa (**_breakpoint_**), de forma que, durante a execução, o programa para nesses pontos;
- Especificar que, toda vez que o conteúdo de uma variável for modificado, o programa envio uma mensagem (**_watchpoint_**)

# Notas
- [[Arquitetura de Sistemas Operacionais - Capítulo 02]]

# Referências

1. MACHADO, F. B.; MAIA L. P. **Arquitetura de Sistemas Operacionais**, 5. ed., Rio de Janeiro: LTC, 2013. ISBN:9788521622109 
2. WIKIPEDIA. **Software**, Acessado em 01/07/2023, Disponível em: <https://pt.wikipedia.org/wiki/Software>