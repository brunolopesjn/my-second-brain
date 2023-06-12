# Arquitetura de Sistemas Operacionais - Capítulo 02

## Seção 2.2 - Hardware
- Um **sistema computacional** é um conjunto de circuitos eletrônicos interligados, formado pro processadores, memórias, registradores, barramentos, monitores de vídeo, impressoras, mouse, discos de armazenamento, além de outros dispositivos físicos (**_hardware_**).
- Todos os componentes de um sistema computacional são agrupados em três subsistemas básicos chamados de **unidades funcionais**:
	- Processador ou Unidade Central de Processamento;
	- Memória principal;
	- Dispositivos de Entrada e Saída.

## Seção 2.2.1 - Processador
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

## Seção 2.2.2 - Memória
- A **memória principal**, **primária** ou **real** é o local onde são armazenados instruções e dados.
- A memória é composta por unidades de acesso chamada de células, sendo cada célula composta por um determinado número de **bits**.
- O **bit** é a unidade básica de memória, podendo assumir o valor lógico **0** ou **1**.
- Atualmente a grande maioria dos computadores utilizam o **byte** (8 bits) como tamanho de célula, porém encontramos computadores de gerações passadas com células de 16, 32 e até 60 bits



# Referências

1. MACHADO, F. B.; MAIA L. P. **Arquitetura de Sistemas Operacionais**, 5. ed., Rio de Janeiro: LTC, 2013. ISBN:9788521622109    