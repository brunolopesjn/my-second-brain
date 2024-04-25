---
title: "Bitcoin: A Peer-to-Peer Eletronic Cash System"
author: Satochi Nakamoto
year: "2009"
bibtex: "@article{nakamoto2009bitcoin,  abstract = {A purely peer-to-peer version of electronic cash would allow online payments to be sent directly from one party to another without going through a financial institution. Digital signatures provide part of the solution, but the main benefits are lost if a trusted third party is still required to prevent double-spending. We propose a solution to the double-spending problem using a peer-to-peer network. The network timestamps transactions by hashing them into an ongoing chain of hash-based proof-of-work, forming a record that cannot be changed without redoing the proof-of-work. The longest chain not only serves as proof of the sequence of events witnessed, but proof that it came from the largest pool of CPU power. As long as a majority of CPU power is controlled by nodes that are not cooperating to attack the network, they'll generate the longest chain and outpace attackers. The network itself requires minimal structure. Messages are broadcast on a best effort basis, and nodes can leave and rejoin the network at will, accepting the longest proof-of-work chain as proof of what happened while they were gone.},  added-at = {2022-06-15T13:43:05.000+0200},  author = {Nakamoto, Satoshi},  biburl = {https://www.bibsonomy.org/bibtex/2974d35fdb27dea57296ed2245556aa18/daniel_grm9},  interhash = {423c2cdff70ba0cd0bca55ebb164d770},  intrahash = {974d35fdb27dea57296ed2245556aa18},  keywords = {itsecseminar},  month = may,  timestamp = {2022-06-15T13:43:05.000+0200},  title = {Bitcoin: A Peer-to-Peer Electronic Cash System},  url = {http://www.bitcoin.org/bitcoin.pdf},  year = 2009}"
---
# Anotações do Manuscrito

## Introdução

- O comercio eletrônico na Internet tem dependido exclusivamente de instituições financeiras que servem como terceiros confiáveis para processar pagamentos eletrônicos. Porém, enquanto o sistema funciona bem para a maioria das operações, sofre com as deficiências do modelo baseado em confiança.
- Um sistema de pagamento baseado em prova criptográfica em vez de confiança é necessário para permitir que quais duas partes dispostas a transacionar diretamente com a outra sem a necessidade de um terceiro confiável.
- Esse sistema baseado em prova criptográfica é seguro desde que os nós honestos controlem coletivamente mais poder de _CPU_ do que qualquer grupo cooperado de nós maliciosos.

## Transações

- Nós (o autor) definimos uma moeda eletrônica como uma cadeia de assinaturas digitais, onde a transferência de um ativo financeiro se dá através da assinatura digital do _hash_ da operação anterior e a chave pública do
- 