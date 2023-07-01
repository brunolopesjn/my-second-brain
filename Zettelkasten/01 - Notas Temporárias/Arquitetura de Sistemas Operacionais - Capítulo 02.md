# Arquitetura de Sistemas Operacionais - Capítulo 02

## Seção 2.2 - Hardware
- Um **sistema computacional** é um conjunto de circuitos eletrônicos interligados, formado pro processadores, memórias, registradores, barramentos, monitores de vídeo, impressoras, mouse, discos de armazenamento, além de outros dispositivos físicos (**_hardware_**).
- Todos os componentes de um sistema computacional são agrupados em três subsistemas básicos chamados de **unidades funcionais**:
	- Processador ou Unidade Central de Processamento;
	- Memória principal;
	- Dispositivos de Entrada e Saída.

### Seção 2.2.1 - Processador
- O **processador** tem como função principal controlar e executar instruções presentes na memória principal, por meio de operações básicas como somar, subtrair, comparar e movimentar dados.
- Cada processador é composto por:
	- Unidade de controle;
	- Unidade lógica e Aritmética;
	- Registradores.
- A **unidade de controle** (UC) é responsável por  gerenciar as atividades de todos os componentes  do computador, como a gravação de dados em discos ou a busca de instruções na memória.
- A **unidade lógica de aritmética** (ULA), como o nome indica, é responsável pela realização de operações lógicas (testes e comparações) e aritméticas (somas e subtrações).
- Os **registradores** são dispositivos com a função principal de armazenar dados temporariamente. O conjunto de registradores funcionam como uma memória de alta velocidade interna do processador, porém com uma capacidade de armazenamento reduzida e custo maior do que o da memória principal.
- Alguns registradores podem ser manipulados  diretamente por instruções (registradores de uso geral), enquanto outros são responsáveis por armazenar informações de controle do processamento e do sistema operacional (registradores de uso específico).
- Entre os registradores de uso específico, merecem destaque:
	- O **contador de instruções** (CI) ou **_program counter_** (PC) contém o endereço da próxima instrução que o processador deve buscar e executar. Toda vez que o processador busca por uma nova instrução, este registrador é atualizado com o endereço de memória da instrução seguinte a ser executada.
	- O **apontador de pilha** (AP) ou **_stack pointer_** (SP) contém o endereço de memória do topo da pilha, que é a estrutura de dados onde o sistema mantém todas as informações sobre o programa que estão sendo executados.
	- O **registrador de instruções** (RI) é responsável por armazenar a instrução que será decodificada e executada pelo processador.
	- O **registrador de status** ou **_program status word_** (PSW) é responsável por armazenar informações sobre a execução de instruções, como a ocorrência de _overflow_. A maioria das instruções, quando executadas, altera o registrador de status conforme o resultado.
- O **ciclo de busca de instrução** é a maneira pela qual o processador executa os programas armazenados na memória principal segundo os passos descritos a seguir:
	1. O processador busca na memória principal a instrução armazenada no endereço indicado pelo CI e a armazena do RI;
	2. O processador incrementa o CI para que o registro contenha o endereço da próxima instrução;
	3. O processador decodifica a instrução armazenada no RI;
	4. O processador busca os operandos na memória, se houver;
	5. O processador executa a instrução decodificada.

### Seção 2.2.2 - Memória
- A **memória principal**, **primária** ou **real** é o local onde são armazenados instruções e dados.
- A memória é composta por unidades de acesso chamada de células, sendo cada célula composta por um determinado número de **bits**.
- O **bit** é a unidade básica de memória, podendo assumir o valor lógico **0** ou **1**.
- Atualmente a grande maioria dos computadores utilizam o **byte** (8 bits) como tamanho de célula, porém encontramos computadores de gerações passadas com células de 16, 32 e até 60 bits.
- Podemos concluir, então, que a memória é formada por um conjunto de células, onde cada célula possui um determinado número de bits.
- O acesso ao conteúdo de uma célula é realizado através da especificação de um número chamado **endereço**.
- O endereço é uma referência única que podemos fazer a uma célula de memória.
- Quando um programa deseja ler ou escrever um dado em uma célula, deve primeiro especificar qual endereço de memória desejado, para depois realizar a operação.
- A memória principal podem ser classificadas em função da sua volatilidade, que é a capacidade de a memória preservar o seu conteúdo mesmo sem uma fonte de alimentação ativa.
	- Memórias do tipo RAM (Random Access Memory) são voláteis , enquanto as memórias ROM (Read-Only Memory) e EPROM (Erasable Programmable ROM) são do tipo não voláteis.

### Seção 2.2.5 - Dispositivos de Entrada e Saída
- Os **dispositivos de entrada e saída** (abreviado como **E/S**) são utilizados para permitir a comunicação entre o sistema computacional e o mundo externo.
- Podem ser divididos em duas categorias: os que servem como memória secundária e os que servem para a interface homem-máquina.
- Os dispositivos  utilizados como memória secundária (discos de armazenamento sólido, discos elétrico-mecânicos e fitas magnéticas) caracterizam-se por ter capacidade de armazenamento bastante superior ao da memória principal.
- Seu custo é relativamente baixo, porém o tempo de acesso à memória secundária é bem superior ao da memória principal.
- Outros dispositivos têm como finalidade a comunicação usuário-maquina, como teclados, mouse, monitores de vídeo e impressoras.
- A implementação de interfaces mais amigáveis permite que pessoas menos especializadas utilizem computadores de maneira intuitiva.

## Seção 2.3 - Software
- Para que o hardware tenha utilidade prática, deve existir um conjunto de programas utilizado como interface entre as necessidades do usuário e as capacidade do hardware.
- A utilização de softwares adequados às diversas tarefas e aplicações torna o trabalho dos usuários muito mais simples e eficiente.

### Seção 2.3.1 - Tradutor
- Nos primeiros sistemas computacionais, o ato de programar um computador era bastante complicado, já que o programador deveria possuir conhecimento da arquitetura da máquina e programar em painéis através de fios.
- Esses programas  eram desenvolvidos em linguagem de máquina e carregados diretamente na memória principal para execução.
- Com o surgimento das primeiras **linguagens de montagem** ou **_assembly_** e das **linguagens de alto nível**, o programador deixou de se preocupar com muitos aspectos pertinentes ao hardware, como em qual região de memória o programa deveria ser carregado ou quais endereços de memória seriam reservados para as variáveis.
- Apesar das inúmeras vantagens das linguagens de montagem e de alto nível, os programas escritos nessas linguagem não estão prontos para ser diretamente executados pelo processador (**programa-fonte**).
- Para isso, eles têm de passar por uma etapa de conversão, onde toda representação simbólica das instruções é traduzida para código de máquina.
- Essa conversão é realizada por um utilitário chamado **tradutor**.
- O módulo gerado pelo tradutor é denominado **módulo-objeto**, que, apesar de estar em código de máquina, na maioria das vezes não pode ser ainda executado.
- Isso ocorre em uma função de um programa poder chamar sub-rotinas externas, e, nesse caso, o tradutor não tem como associar o programa principal às sub-rotinas chamadas.
- Dependendo do tipo do programa-fonte, existem dois tipos de tradutores que geram código objeto:
	- O **montador** (**_assembler_**) é o utilitário responsável por traduzir um programa fonte em linguagem de montagem em um programa-objeto não executável. A linguagem de montagem é particular para cada processador, assim como a linguagem de máquina, o que não permite que programas _assembly_ serem portados entre máquinas diferentes.
	- O **compilador** é o utilitário responsável por gerar, a partir de um programa escrito em uma linguagem de alto nível, um programa de linguagem de máquina não executável. As linguagens de alto nível, como Pascal, FORTRAN e COBOL, não têm nenhuma relação direta com a máquina, ficando essa preocupação exclusivamente com o compilador.

### Seção 2.3.1 - Interpretador
- A partir da execução de um programa-fonte escrito em linguagem de alto nível, o interpretador, durante a execução do programa, traduz cada instrução e a executa imediatamente. Algumas linguagens tipicamente interpretadas são o Basic e o Perl.
- A maior desvantagem no uso de interpretadores é o tempo gasto na tradução das instruções de um programa toda vez que este for executado, já que não existe a geração de um código executável.
- A vantagem é permitir a implementação de tipos de dados dinâmicos, ou seja, que podem mudar de tipo durante a execução do programa, aumentando, assim, sua flexibilidade.

### Seção 2.3.3 - Linker

O **_linker_** ou **editor de ligação** é o utilitá

### Seção 2.3.4 - Loader


### Seção 2.3.5 - Depurador
- O desenvolvimento de programas está sujeito a erros de lógica, independente de metodologias utilizadas pelo programador.
- A depuração é um dos estágios desse desenvolvimento, é a utilização de ferramentas adequadas é essencial para acelerar o processo de correção dos programas.
- O depurador (_debugger_) é o utilitário que permite ao usuário acompanhar toda a execução de um programa a fim de detectar erros na sua lógica.
- Esse utilitário oferece ao usuário recursos como:
	- acompanhar a execução de um programa instrução por instrução;
	- possibilitar a alteração e a visualização do conteúdo de variáveis;
	- implementar pontos de parada dentro do programa (_breakpoint_), de forma que, durante a execução, o programa para nesses pontos;
	- especificar que, toda vez que o conteúdo de uma variável for modificado, o programa envie uma mensagem (_watchpoint_)

# Referências

1. MACHADO, F. B.; MAIA L. P. **Arquitetura de Sistemas Operacionais**, 5. ed., Rio de Janeiro: LTC, 2013. ISBN:9788521622109 