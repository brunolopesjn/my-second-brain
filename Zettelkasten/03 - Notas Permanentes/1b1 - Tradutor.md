# Tradutor

Nos primeiros sistemas computacionais, o ato de programar um computador era bastante complicado, já que a pessoa programadora deveria possuir conhecimento da arquitetura do sistema computacional e programa-lo através de painéis utilizando fios. Esses programas eram desenvolvidos em linguagem de máquina e carregados diretamente na memória principal para execução.

Com o surgimento das primeiras **linguagens de montagem** ou **_assembly_** e das **linguagens de alto nível**, o programador deixou de se preocupar com muitos aspectos pertinentes ao hardware como, por exemplo, em qual região de memória o programa deveria ser carregado ou quais endereços de memória seriam reservados para as variáveis.

Apesar das inúmeras vantagens das linguagens de montagem e de alto nível, os programas escritos nessas linguagens , chamados de **programa-fonte**, não estão prontos para serem diretamente executados pelo processador.

Para isso, eles têm de passar por uma etapa de conversão, onde toda representação simbólica das instruções é traduzida para código de máquina. Essa conversão é realizada por um utilitário de software chamado **tradutor**.

O módulo gerado pelo tradutor é denominado **módulo-objeto**, que, apesar de estar em código de máquina, na maioria das vezes não pode ser executado ainda. Isso ocorre em uma função de um programa poder realizar chamadas a sub-rotinas externas e, nesse caso, o tradutor não tem como associar o programa principal às sub-rotinas chamadas.

# Referências

1. [[Zettelkasten/02 - Notas de Literatura/O que é um Computador?|O que é um Computador?]]