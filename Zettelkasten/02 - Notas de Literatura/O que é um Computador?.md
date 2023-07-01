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

Para que o hardware tenha utilidade prática, deve existir um conjunto de programas que servem como interface entre as necessidades das pessoas que utilizam um computador e as capacidades do hardware em uso.

Um programa é composto por uma sequência de instruções, que podem ser em linguagem natural ou codificada (linguagem de programação), que é interpretada e executada por um processador ou por uma máquina virtual.

O termo **software** foi criado na década de 1940, e é um trocadilho com o termo **hardware** que, em inglês

### Tradutor

### Interpretador

#### Linker

#### Loader

#### Depurador

# Referências

1. MACHADO, F. B.; MAIA L. P. **Arquitetura de Sistemas Operacionais**, 5. ed., Rio de Janeiro: LTC, 2013. ISBN:9788521622109 