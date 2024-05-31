# Proof of Work

O _Proof of Work _(PoW) é um mecanismo de _timestamp_ distribuído em uma rede _peer-to-peer_ que utiliza um sistema similar ao _Hashcash_ de _Adam Back_. Esse mecanismo envolve a procura de um valor de _hash_ do bloco que comece com uma quantidade de bits zero.

O trabalho computacional necessário para encontrar um _hash_ que inicie com uma quantidade de bits zero é exponencial a própria quantidade de bits zero e para verificar a validade desse _hash_ basta simplesmente gerar um _hash_ com os valores do bloco, ou seja, leva-se um tempo considerável para gerar o _hash_ mas é rápido para validar a sua autenticidade.

No Bitcoin foi implementado o campo _nonce_ (number used once) o qual é incrementado até que seja obtido um _hash_ com a quantidade de bits zero requeridos. Uma vez que se tenha encontrado um _hash_ válido através do _PoW_, o bloco não pode ser modificado sem realizar todo esse trabalho novamente, pois como todos os blocos são encadeados através do _hash_ posterior, o trabalho de alterar um bloco requer recalcular todos os _hash_ após ele.

O _PoW_ também resolve o problema da tomada de decisão pela maioria. A decisão da maioria é representada pela cadeia de blocos mais longa que, consequentemente, possui o maior esforço de prova de trabalho investido nela. Logo se a maioria de poder de CPU ou GPU é controlado pelos nós honestos, a cadeia honesta crescerá rápido e superará quaisquer cadeias concorrentes.

Para compensar o aumento da velocidade de hardware e o interesse variado em executar vários nós ao longo do tempo, a dificuldade da prova de trabalho é determinada por uma média móvel visando um número médio de blocos por hora, ou seja, se eles forem gerados muito rápido, a dificuldade aumenta.

## Tags

#bitcoin #blockchain 

## Veja também

[[Bitcoin]]
[[Blockchain]]