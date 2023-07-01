# Loader

O **_loader_** ou **carregador** é o utilitário responsável por carregar na memória principal um programa para ser executado. O procedimento de carga varia com o código gerado pelo **linker** e, em função deste, o **loader** é classificado como do tipo **absoluto** ou **relocável**.

Se o código fonte dor do tipo absoluto, o _loader_ só necessita conhecer o endereço de memória inicial e o tamanho do módulo para realizar o carregamento. Então, o _loader_ transfere o programa da memória secundária para a memória principal e inicia a sua execução (**_loader_ absoluto**).

No caso do código relocável, o programa pode ser carregado em qualquer posição de memória , e o _loader_ é responsável pela realozação no momento do carregamento (**_loader_ relocável**).

# Referências

1. [[Zettelkasten/02 - Notas de Literatura/O que é um Computador?|O que é um Computador?]]