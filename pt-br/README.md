# KCC

## Introdu��o
KCC � uma cadeia p�blica descentralizada e de alto desempenho constru�da pelas comunidades de f�s da KCS e KuCoin.

Desenvolvido com base no go-ethereum com o objetivo de fornecer aos usu�rios da comunidade uma velocidade mais alta,
experi�ncia de usu�rio blockchain conveniente e de baixo custo.

O KCC ter� as seguintes caracter�sticas:
- Totalmente compat�vel com contratos inteligentes Ethereum e ERC-20, com custos de migra��o extremamente baixos;
- KCS servir� como o �nico combust�vel principal e token nativo para KCC e pode ser usado em cen�rios como pagamento de taxa de g�s;
- Um bloqueio a cada 3 segundos resulta em confirma��o de transa��o mais r�pida e maior desempenho da cadeia;
- Algoritmo de consenso Proof of Staked Authority (PoSA), alta efici�ncia, seguran�a e estabilidade.

## Miss�o

Miss�o: Acelerar o fluxo de valor ao redor do mundo sem fronteiras.

## Declara��o de risco

- O KCC oficialmente n�o lan�ar� nenhum projeto Swap porque todos os projetos s�o desenvolvidos pela comunidade. Portanto, o KCC n�o se responsabiliza por qualquer inconveniente causado por esses projetos. Al�m disso, o KCC n�o serve como atendimento ao cliente para projetos relevantes.
- Antes de qualquer opera��o nos campos relacionados � criptomoeda ou DeFi, primeiro fa�a sua pr�pria pesquisa.
- Todos os usu�rios e desenvolvedores podem construir o dApp na rede de teste KCC e depois na rede principal no acompanhamento gratuitamente.
- Por favor, diferencie o ambiente de teste (o testnet) do ambiente de rede principal (o mainnet). Os ativos gerados no ambiente de teste n�o t�m valor, portanto, tome cuidado com a fraude de criptomoedas.
- A KCC anunciar� autoriza��o, promo��o e outras coopera��es atrav�s de sua rede social oficial, por favor, verifique as informa��es oficiais e evite sites de phishing.
- Certifique-se de estar visitando o site oficial para evitar a perda da chave privada.

## Isen��es de responsabilidade
Caro usu�rio (doravante referido como "voc�"):

A KCC (doravante denominada "KCC" ou "n�s") � uma cadeia p�blica descentralizada. Desenvolvedores de todo o mundo podem implantar aplicativos no KCC, todos os usu�rios podem ler, enviar e negociar no KCC. Devido �s caracter�sticas da descentraliza��o, lembramos que os riscos do DAPP de terceiros s�o os seguintes:

- Antes de operar em qualquer plataforma, carteira ou DAPP de terceiros, fa�a sua pr�pria pesquisa primeiro;
- Se voc� participa ou usa DAPP no KCC por meio de qualquer plataforma de negocia��o ou carteira, � seu pr�prio comportamento e n�o o recomendamos a voc�;
- N�o nos responsabilizamos por auditar qualquer DAPP de terceiros, nem assumimos qualquer compromisso e garantia sobre a validade, exatid�o, exatid�o, confiabilidade, qualidade, estabilidade, integridade e pontualidade da tecnologia e informa��es envolvidas em seus servi�os;
- Voc� deve arcar com todas as responsabilidades decorrentes do uso de quaisquer servi�os DAPP de terceiros por conta pr�pria;
- Se os servi�os DAPP de terceiros atendem �s leis, regulamentos ou pol�ticas relevantes de sua jurisdi��o, fa�a seu pr�prio julgamento e avalia��o. N�s n�o fornecemos qualquer avalia��o, por favor, certifique-se de cumprir rigorosamente as leis de sua jurisdi��o;
- Voc� e o DAPP de terceiros devem assumir as responsabilidades de quaisquer quest�es relacionadas ao uso do DAPP de terceiros, incluindo, mas n�o limitado a, quest�es legais, quest�es de responsabilidade contratual, perdas econ�micas, etc., a KCC n�o ser� respons�vel por eles;
- A menos que voc� nos autorize a faz�-lo, a KCC n�o compartilhar� suas informa��es pessoais com nenhum DAPP de terceiros. Se voc� nos autorizar a compartilhar as informa��es, todas as responsabilidades legais e disputas decorrentes do acesso do DAPP de terceiros �s suas informa��es pessoais ser�o assumidas por voc� e pelo DAPP de terceiros.
- A KCC n�o tem o direito de fornecer informa��es pessoais de quaisquer desenvolvedores de DAPP de terceiros, a menos que eles concordem em faz�-lo. Ajudaremos nessa quest�o, mas n�o podemos garantir que as informa��es possam ser obtidas.

Por fim, precisamos reiterar que n�o recomendamos ou solicitamos que voc� use nenhum servi�o DAPP de terceiros.

# Par�metros de rede
Os usu�rios da comunidade podem usar qualquer carteira compat�vel com Ethereum para configurar com par�metros de rede KCC, como [metamask](https://metamask.io/), [myetherwallet](https://www.myetherwallet.com/), [imtoken]( https://token.im/), [TokenPocket](https://www.tokenpocket.pro/) etc.

## Rede principal
```
Nome da cadeia: KCC-MAINNET
ID da cadeia: 321
S�mbolo: KCS
URL RPC: https://rpc-mainnet.kcc.network
URL do explorador: https://explorer.kcc.io/en
URL de RPC do WebSocket: wss://rpc-ws-mainnet.kcc.network
```

*O limite de taxa do endpoint na Testnet e Mainnet � 300/10s*

*Os usu�rios tamb�m podem usar [https://scan.kcc.io](https://scan.kcc.io) como Block Explorer.*

## Rede de teste
```
Nome da cadeia: KCC-TESTNET
ID da cadeia: 322
S�mbolo: KCS
URL RPC: https://rpc-testnet.kcc.network
URL do Explorer: https://scan-testnet.kcc.network
URL de RPC do WebSocket: wss://rpc-ws-testnet.kcc.network

URL da torneira: https://faucet-testnet.kcc.network (apenas para teste, sem valor)
```

# Desenvolvedor

## N�
### Arquivo bin�rio
Voc� pode visitar diretamente [https://github.com/kcc-community/kcc/releases](https://github.com/kcc-community/kcc/releases) para baixar a vers�o mais recente do arquivo bin�rio?

### Docker
Ou voc� pode visitar [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) para implanta��o e teste r�pidos?([How to use Docker ?](https://docs.docker.com/get-started/))

### Compila��o
#### Requisitos
- Linux ou Mac
- golang >= 1,13
- git

[como baixar e instalar golang](https://golang.org/doc/install)

#### Degraus
```
git clone -b kcc --single-branch https://github.com/kcc-community/kcc.git
cd kcc
fazer geth
```
#### Correndo
Os sinalizadores de linha de comando s�o semelhantes ao go-ethereum, voc� pode usar `./build/bin/geth --help` para todas as op��es de linha de comando,
como `./build/bin/geth --testnet` para entrar na Testnet. Cuidado: Use a vers�o "geth" espec�fica localizada em `./build/bin/geth`.

## Docker

Voc� pode usar [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) para implantar e testar rapidamente.

[Como usar o Docker?](https://docs.docker.com/get-started/)

## Implantar

### Requisitos
```
CPU de 4 n�cleos
8g de mem�ria
SSD de 200G e escal�vel
IP p�blico com TCP/UDP:30303 aberto
```

#### Comando de partida
```
./geth #Mainnet
./geth --testnet #Testnet

op��es �teis:
/data/kcc/get\
--datadir /data/.kcc/testnet \ #seu diret�rio de dados
--testnet \ #Testnet
--http\#http rpc
--http.addr 0.0.0.0 \ #http rpc endere�o de liga��o
--http.vhosts * \ #vhosts
--http.corsdomain * \ #http corsdomain
--ws \ #ws rpc
--ws.addr 0.0.0.0 \ #ws rpc endere�o de liga��o
--syncmode completo \ #syncmode
--gcmode arquivo #gcmode
```

Voc� pode usar `nohup`,`supervisor`,`systemd` para executar e gerenciar `geth` em segundo plano.

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDK
Voc� pode usar os seguintes SDKs para interagir com o rpc do n� KCC.

- [Js: web3.js](https://github.com/ChainSafe/web3.js) API JavaScript Ethereum
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum �app API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) Uma interface php para interagir com o blockchain e ecossistema Ethereum.
- [Python: Web3.py](https://github.com/ethereum/web3.py) Uma biblioteca Python para interagir com o Ethereum, inspirada no web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## Ferramentas
- [Solidity](https://docs.soliditylang.org/en/latest/)
- [Remix](https://remix.ethereum.org/)
- [Truffle](https://www.trufflesuite.com/docs/trufa/overview)
- [Hardhat](https://hardhat.org/)
- [Faucet](https://faucet-testnet.kcc.network)
- [Explorer](https://explorer.kcc.io)

## Ponte
- [KCC-Bridge](https://www.kcc.io/bridge/transfer/)
- [AnySwap](https://anyswap.exchange/bridge)
## Consenso
KCC introduz um mecanismo de consenso PoSA, que apresenta baixos custos de transa��o, baixo atraso de transa��o,
alta simultaneidade de transa��es e suporta at� 29 validadores.

PoSA � uma combina��o de PoA e PoS. Para se tornar um validador, voc� precisa primeiro enviar uma proposta e esperar que outros validadores ativos votem nela. Ap�s mais da metade deles votarem, voc� estar� apto a se tornar um validador. Qualquer endere�o pode apostar em um endere�o que se qualifique para se tornar um validador e, depois que o volume de staking do validador estiver entre os 29 primeiros, ele se tornar� um validador ativo na pr�xima �poca.

Todos os validadores ativos s�o ordenados de acordo com regras predefinidas e se revezam nos blocos de minas. Se um validador falhar em minerar um bloco a tempo durante sua pr�pria rodada, os validadores ativos que n�o estiveram envolvidos nos �ltimos n/2 blocos (n � o n�mero de validadores ativos) realizar�o o bloqueio aleatoriamente. Pelo menos n/2+1 validadores ativos funcionam corretamente para garantir o bom funcionamento do blockchain.

O valor de dificuldade de um bloco � 2 quando o bloco � gerado normalmente e 1 quando o bloco n�o � gerado em uma ordem pr�-definida. Quando ocorre um fork do blockchain, o blockchain seleciona o fork correspondente de acordo com a dificuldade m�xima acumulada.

### Contratos do Sistema
A KCC fez 3 contratos integrados para PoSA no arquivo genesis.

O c�digo-fonte desses contratos � bifurcado do Heco, voc� pode localiz�-los aqui: [https://github.com/kcc-community/kcc-genesis-contracts](https://github.com/kcc-community/kcc -genesis-contratos)?

A gest�o dos validadores atuais � toda feita pelos contratos do sistema.

- Proposta Respons�vel por gerenciar o acesso aos validadores e gerenciar as propostas e votos dos validadores.
- Validadores Respons�vel pela gest�o do ranking de validadores, opera��es de staking e untaking, distribui��o de recompensas em bloco, etc.
- Punir Respons�vel por punir opera��es contra validadores ativos que n�o estejam funcionando corretamente.

Contratos do sistema de chamadas Blockchain:

- Ao final de cada bloco, o contrato de Validadores � chamado e as taxas de todas as transa��es do bloco s�o distribu�das aos validadores ativos.
- O contrato Punir � chamado para punir o validador quando o validador n�o estiver funcionando corretamente.
- Ao final de cada �poca, o contrato de Validadores � chamado para atualizar os validadores ativos, com base no ranking.

### estaca
Voc� pode chamar o m�todo `stake` no contrato `validator` para apostar para qualquer validador, o valor m�nimo de aposta para cada validador � 32KCS.

### desmarcar
Se voc� quiser `unstake` seu KCS, voc� precisa chamar o m�todo `unstake` no contrato `validator`,
e aguarde 86.400 blocos (3 dias), ent�o chame o m�todo `withdrawStaking` no contrato `validator` para disponibilizar o valor.

### punir
Sempre que um validador n�o minerar um bloco como pr�-definido, o contrato Punish � automaticamente chamado ao final deste bloco e o validador � contabilizado. Quando a contagem chega a 24, todos os rendimentos do validador s�o punidos. Quando a contagem atinge 48, o validador � removido da lista de validadores ativos e o validador � desclassificado.

## O gr�fico
O Graph Node � um protocolo para criar aplicativos descentralizados (dApps) rapidamente no Ethereum e IPFS usando o GraphQL.

O n� Graph aberto pela equipe de desenvolvimento da comunidade KCC s�o:
```
https://thegraph.kcc.network/deploy/
https://thegraph.kcc.network/ipfs/
https://thegraph.kcc.network/subgraphs/name/
```

Exemplo:
```
"auth": "autentica��o do gr�fico https://thegraph.kcc.network/deploy/ your-token"
"create": "graph create your-name --node https://thegraph.kcc.network/deploy/"
"deploy": "graph deploy your-name --ipfs https://thegraph.kcc.network/ipfs/ --node https://thegraph.kcc.network/deploy/"
"explorer": "https://thegraph.kcc.network/subgraphs/name/your-name"
```

**Se precisar usar o servi�o, preencha o [formul�rio de inscri��o](https://forms.office.com/r/DQawaDHtnF)**

**Devido a problemas de desempenho, recomendamos que voc� siga [The Graph the Official document](https://thegraph.com/docs/) e fa�a a implanta��o da privatiza��o e implante seu pr�prio n�.**


# Governan�a

## Conselhos, quest�es e discuss�es

Qualquer conselho, quest�es e discuss�o s�o bem-vindos.

[Deixe um conselho ou um problema](https://github.com/kcc-community/any-advice-issue/issues)

[Iniciar uma discuss�o](https://github.com/kcc-community/any-advice-issue/discussions)

Se voc� tiver um problema em um projeto especial, v� para a p�gina "problema" no projeto especial.


## KIP
Propostas de melhoria do KCC

As propostas de melhoria KCC (KIPs) descrevem os padr�es para a plataforma KCC, incluindo Chain, DEX e dApps.

O objetivo deste processo � garantir que as mudan�as no KCC sejam transparentes e bem governadas.

URL:[https://github.com/kcc-community/KIPs](https://github.com/kcc-community/KIPs)

# PERGUNTAS FREQUENTES
1. Qual � o mecanismo de consenso do KCC?

>KCC adota o mecanismo de consenso PoSA, apresentando baixo custo, alto desempenho e gera��o de blocos est�vel, suportando at� 29 validadores;
2.Como se tornar um n� validador KCC?

>Para se tornar um validador, voc� precisa criar um n� e enviar uma proposta, e aguardar a vota��o de outros validadores ativos. Depois de receber mais da metade dos votos, voc� � eleg�vel para se tornar um validador. Qualquer endere�o pode apostar no endere�o que � eleg�vel para se tornar um validador. Depois que o valor apostado do validador estiver entre os 29 primeiros, o validador se tornar� ativo na pr�xima �poca.

3. O KCC suporta EVM?

>KCC suporta totalmente EVM e � totalmente amig�vel para desenvolvedores de Ethereum.

4.Qual SDK o KCC usa?

> O KCC � altamente compat�vel com o Ethereum, ent�o adotamos o SDK do Ethereum, como web3js, web3j, etc.

5.Quero realizar algumas opera��es e testes na rede de teste KCC. Onde posso obter tokens de teste?

>Voc� pode visitar nossa torneira testnet: https://faucet-testnet.kcc.network.

6.Como apostar n�s de contrato?

>Os usu�rios podem chamar o m�todo stake do contrato do validador para fazer o stake de qualquer n�. O valor m�nimo apostado para cada validador � de 32 KCS.

7.Como desbloquear o valor apostado?

>Se os usu�rios quiserem recuperar o KCS apostado, eles precisam chamar o m�todo untake do contrato dos validadores para desbloquear o valor apostado. Ap�s a gera��o de 86.400 blocos (3 dias), chame o m�todo retiroStaking do contrato dos validadores para recuperar o KCS apostado.

8. Ficar preso ao usar o MetaMask (incluindo, mas n�o limitado a transfer�ncia travada ou atrasada, problema de exibi��o de dados, etc.)

>Use a visualiza��o de expans�o do plug-in para exibir em tela cheia, que pode ser mais est�vel ou escolha "Acelerar" para aumentar o gaslimt e o gasPrice.

9. Como usar a ponte KCC para o servi�o de convers�o de ativos de cadeia cruzada?

> Voc� pode consultar nosso tutorial em v�deo: https://www.youtube.com/watch?v=kZdX1V2Tgnc

>Para mais tutoriais, assine nosso canal do Youtube: https://www.youtube.com/channel/UCZhWm40SuAApnLqqq3F9o1w

10. O que acontece se usarmos KCC em vez de ERC20 ao enviar Tether para um endere�o que n�o suporta KCC? Ele se recupera depois de um certo per�odo de tempo?

> Se o endere�o de destino for o seu endere�o pessoal, a opera��o � bastante simples. Altere a rede da carteira para KCC e importe seu endere�o e seu endere�o de contrato KCC-USDT, ent�o voc� poder� ver o saldo do USDT.

>Se o seu endere�o de destino for uma bolsa ou uma carteira centralizada, voc� precisa entrar em contato com o suporte ao cliente para permitir que eles suportem o KCC ou reembols�-los para seu endere�o original.

> Portanto, sugerimos que nossos usu�rios sejam claros sobre o motivo pelo qual far�o a transfer�ncia, j� que o blockchain possui imutabilidade, o que significa que qualquer transfer�ncia n�o pode ser revertida uma vez enviada, e sempre recomendamos primeiro tentar com uma quantidade menor.


## Como configurar a carteira MetaMask

Use o navegador Chrome para abrir o MetaMask [site de extens�o](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

Siga a introdu��o, crie sua carteira ETH,**fa�a backup de sua chave privada ou mnem�nico**;

Configurar rede principal KCC

(1) Abra o MetaMask,voc� pode ver a configura��o padr�o da?Ethereum mainnet?

<img width="170" alt="E1" src="https://user-images.githubusercontent.com/13411690/121641021-3f093900-cac1-11eb-9c06-fd653cd598a1.png">


clique em?Ethereum mainnet?,clique em?Custom RPC?no menu suspenso

<img width="170" alt="E2" src="https://user-images.githubusercontent.com/13411690/121641049-4597b080-cac1-11eb-8674-3755c30a3398.png">


(2) Preencha esse valor de configura��o para mudar para o KCC Mainnet:

    Nome da rede: KCC-MAINNET
    
    Nova URL RPC: https://rpc-mainnet.kcc.network
    
    ID da cadeia: 321
    
    S�mbolo de moeda (opcional): KCS
    
    URL do Explorador de Blocos (opcional): https://explorer.kcc.io/en

<img width="170" alt="E3" src="https://user-images.githubusercontent.com/13411690/121641889-598fe200-cac2-11eb-92c5-6617c103ebee.png">




Feito

<img width="170" alt="E4" src="https://user-images.githubusercontent.com/13411690/121641085-51837280-cac1-11eb-80cd-1a208c0bcd54.png">

## Como desbloquear transa��es travadas no MetaMask?
[[V�deo]Como desbloquear transa��es bloqueadas no MetaMask (KCC)](https://youtu.be/0xkkRmajIJI)

## Como adicionar um token personalizado � sua carteira MetaMask?
[[V�deo]Como adicionar um token personalizado � sua carteira MetaMask (KCC)](https://youtu.be/tb7xSLur6EU)

