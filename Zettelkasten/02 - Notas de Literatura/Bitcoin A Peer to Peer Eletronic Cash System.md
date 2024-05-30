---
title: "Bitcoin: A Peer-to-Peer Eletronic Cash System"
author: Satochi Nakamoto
year: "2009"
bibtex: "@article{nakamoto2009bitcoin,  abstract = {A purely peer-to-peer version of electronic cash would allow online payments to be sent directly from one party to another without going through a financial institution. Digital signatures provide part of the solution, but the main benefits are lost if a trusted third party is still required to prevent double-spending. We propose a solution to the double-spending problem using a peer-to-peer network. The network timestamps transactions by hashing them into an ongoing chain of hash-based proof-of-work, forming a record that cannot be changed without redoing the proof-of-work. The longest chain not only serves as proof of the sequence of events witnessed, but proof that it came from the largest pool of CPU power. As long as a majority of CPU power is controlled by nodes that are not cooperating to attack the network, they'll generate the longest chain and outpace attackers. The network itself requires minimal structure. Messages are broadcast on a best effort basis, and nodes can leave and rejoin the network at will, accepting the longest proof-of-work chain as proof of what happened while they were gone.},  added-at = {2022-06-15T13:43:05.000+0200},  author = {Nakamoto, Satoshi},  biburl = {https://www.bibsonomy.org/bibtex/2974d35fdb27dea57296ed2245556aa18/daniel_grm9},  interhash = {423c2cdff70ba0cd0bca55ebb164d770},  intrahash = {974d35fdb27dea57296ed2245556aa18},  keywords = {itsecseminar},  month = may,  timestamp = {2022-06-15T13:43:05.000+0200},  title = {Bitcoin: A Peer-to-Peer Electronic Cash System},  url = {http://www.bitcoin.org/bitcoin.pdf},  year = 2009}"
---
# Anotações do Manuscrito

## Introduction

- O comercio eletrônico na Internet tem dependido exclusivamente de instituições financeiras que servem como terceiros confiáveis para processar pagamentos eletrônicos. Porém, enquanto o sistema funciona bem para a maioria das operações, sofre com as deficiências do modelo baseado em confiança.
- Um sistema de pagamento baseado em prova criptográfica em vez de confiança é necessário para permitir que quais duas partes dispostas a transacionar diretamente com a outra sem a necessidade de um terceiro confiável.
- Esse sistema baseado em prova criptográfica é seguro desde que os nós honestos controlem coletivamente mais poder de _CPU_ do que qualquer grupo cooperado de nós maliciosos.

## Transactions

- Nós (o autor) definimos uma moeda eletrônica como uma cadeia de assinaturas digitais, onde a transferência da moeda se dá através da assinatura digital do _hash_ da operação anterior e da chave pública do novo proprietário adicionando o resultado dessa operação no fim da moeda.
- É possível verificar as assinaturas para validar a cadeia de propriedade, mas não é possível verificar se uma das partes não realizou o **gasto duplo** (uma mesma pessoa gastar a mesma moeda duas ou mais vezes em transações distintas).
- Uma solução comum é a introdução de uma autoridade monetária confiável, que verifique o gasto duplo para todas as transações. O problema desta solução é que o destino de todo o sistema monetário depende da empresa ou governo que gerencia essa autoridade monetária.
- É necessário criar um mecanismo que permita verificar se os antigos detentores da moeda realizaram alguma outra transação envolvendo essa mesma moeda. Para o nosso propósito, a transação mais antiga é a que vale, desta maneira não nos importamos com as tentativas posteriores de gasto duplo.
- Para permitir este tipo de validação sem depender de uma autoridade monetária, é necessário que todas as transações sejam anunciadas publicamente e também é necessário um sistema no qual todas as pessoas participantes concordem com um histórico único da ordem de realização das transações recebidas.
- Uma pessoa que esteja recebendo uma moeda necessita ter a certeza de que no momento em que ocorre uma transação a maioria das outras pessoas (ou nós) participantes concordam que esta moeda foi transacionada pela primeira vez pelo proprietário anterior.

## Timestamp Server

- Tem como objetivo gerar um _hash_ de validação de um bloco de itens e publicar publicamente e amplamente esse  _hash_ a todos os nós.

## Proof of Work

- Para implementar um mecanismo distribuído de _timestamp_ em uma rede _peer-to-peer_, será necessário utilizar um sistema de **prova de trabalho** semelhando ao _Hashcash_ de Adam Back.
- Esse mecanismo envolve a procura por um valor que quando calculado o _hash_ o mesmo comece com um número de bits zero.
- A média do trabalho requerida é exponencial ao número de bits zeros requeridos e pode ser verificada por meio da execução de um único _hash_, ou seja, leva-se um tempo considerável para gerar o _hash_ mas é rápido para validar sua autenticidade.
- No _Bitcoin_ foi implementado a prova de trabalho incrementando um campo _nonce_ (_number used once_) ate que seja encontrada uma quantidade de bits zero.
- Uma vez que que se tenha obtido um _hash_ válido através da prova de trabalho, o bloco não pode ser alterado sem refazer este trabalho.
- Como os demais blocos são encadeados através do _hash_ posteriormente, o trabalho de alterar um bloco requer recalcular todos os _hash_ após ele.
- A prova por trabalho também resolve o problema da tomada de decisão pela maioria. Se a maioria fosse baseada em **um endereço IP um voto** a rede poderia ser subvertida por qualquer pessoa capaz de alocar muitos endereços IPs. Contudo a prova de trabalho é, essencialmente **uma CPU um voto**.
- A decisão da maioria é representada pela cadeia mais longa que, consequentemente, possui o maior esforço de prova de trabalho investido nela.
- Logo se a maioria do poder de CPU é controlado por nos honestos, a cadeia honesta crescerá rápido e superará quaisquer cadeias concorrentes.
- Para compensar o aumento da velocidade de hardware e o interesse variado em executar vários nós ao longo do tempo, a dificuldade da prova de trabalho é determinada por uma média móvel visando um número médio de blocos por hora, ou seja, se eles forem gerados muito rápido, a dificuldade aumenta.

## Rede
- Os passos para executar a rede são os seguinte:
	1. Novas transações são transmitidas para todos os nós;
	2. Cada nó coleta novas transações em um bloco;
	3. Cada nó trabalha para encontrar um _hash_ através da prova de trabalho desafiadora;
	4. Quando um nó encontra uma prova de trabalho, ele transmite o bloco para todos os nós;
	5. Os nós aceitam o bloco somente se todas as transações existentes no bloco forem válidas e que as moedas utilizadas não foram gastas anteriormente (evitar o gasto duplo)
	6. Os nós expressam sua aceitação do bloco trabalhando na criação do próximo bloco na cadeia, utilizando o _hash_ do blo