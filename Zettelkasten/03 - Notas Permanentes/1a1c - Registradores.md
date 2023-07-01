# Registradores

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


# Referências

1. [[Zettelkasten/02 - Notas de Literatura/O que é um Computador?|O que é um Computador?]]