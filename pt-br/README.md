# KCC

## Introdução
KCC é uma cadeia pública descentralizada e de alto desempenho construída pelas comunidades de fãs da KCS e KuCoin.

Desenvolvido com base no go-ethereum com o objetivo de fornecer aos usuários da comunidade uma velocidade mais alta,
experiência de usuário blockchain conveniente e de baixo custo.

O KCC terá as seguintes características:
- Totalmente compatível com contratos inteligentes Ethereum e ERC-20, com custos de migração extremamente baixos;
- KCS servirá como o único combustível principal e token nativo para KCC e pode ser usado em cenários como pagamento de taxa de gás;
- Um bloqueio a cada 3 segundos resulta em confirmação de transação mais rápida e maior desempenho da cadeia;
- Algoritmo de consenso Proof of Staked Authority (PoSA), alta eficiência, segurança e estabilidade.

## Missão

Missão: Acelerar o fluxo de valor ao redor do mundo sem fronteiras.

## Declaração de risco

- O KCC oficialmente não lançará nenhum projeto Swap porque todos os projetos são desenvolvidos pela comunidade. Portanto, o KCC não se responsabiliza por qualquer inconveniente causado por esses projetos. Além disso, o KCC não serve como atendimento ao cliente para projetos relevantes.
- Antes de qualquer operação nos campos relacionados à criptomoeda ou DeFi, primeiro faça sua própria pesquisa.
- Todos os usuários e desenvolvedores podem construir o dApp na rede de teste KCC e depois na rede principal no acompanhamento gratuitamente.
- Por favor, diferencie o ambiente de teste (o testnet) do ambiente de rede principal (o mainnet). Os ativos gerados no ambiente de teste não têm valor, portanto, tome cuidado com a fraude de criptomoedas.
- A KCC anunciará autorização, promoção e outras cooperações através de sua rede social oficial, por favor, verifique as informações oficiais e evite sites de phishing.
- Certifique-se de estar visitando o site oficial para evitar a perda da chave privada.

## Isenções de responsabilidade
Caro usuário (doravante referido como "você"):

A KCC (doravante denominada "KCC" ou "nós") é uma cadeia pública descentralizada. Desenvolvedores de todo o mundo podem implantar aplicativos no KCC, todos os usuários podem ler, enviar e negociar no KCC. Devido às características da descentralização, lembramos que os riscos do DAPP de terceiros são os seguintes:

- Antes de operar em qualquer plataforma, carteira ou DAPP de terceiros, faça sua própria pesquisa primeiro;
- Se você participa ou usa DAPP no KCC por meio de qualquer plataforma de negociação ou carteira, é seu próprio comportamento e não o recomendamos a você;
- Não nos responsabilizamos por auditar qualquer DAPP de terceiros, nem assumimos qualquer compromisso e garantia sobre a validade, exatidão, exatidão, confiabilidade, qualidade, estabilidade, integridade e pontualidade da tecnologia e informações envolvidas em seus serviços;
- Você deve arcar com todas as responsabilidades decorrentes do uso de quaisquer serviços DAPP de terceiros por conta própria;
- Se os serviços DAPP de terceiros atendem às leis, regulamentos ou políticas relevantes de sua jurisdição, faça seu próprio julgamento e avaliação. Nós não fornecemos qualquer avaliação, por favor, certifique-se de cumprir rigorosamente as leis de sua jurisdição;
- Você e o DAPP de terceiros devem assumir as responsabilidades de quaisquer questões relacionadas ao uso do DAPP de terceiros, incluindo, mas não limitado a, questões legais, questões de responsabilidade contratual, perdas econômicas, etc., a KCC não será responsável por eles;
- A menos que você nos autorize a fazê-lo, a KCC não compartilhará suas informações pessoais com nenhum DAPP de terceiros. Se você nos autorizar a compartilhar as informações, todas as responsabilidades legais e disputas decorrentes do acesso do DAPP de terceiros às suas informações pessoais serão assumidas por você e pelo DAPP de terceiros.
- A KCC não tem o direito de fornecer informações pessoais de quaisquer desenvolvedores de DAPP de terceiros, a menos que eles concordem em fazê-lo. Ajudaremos nessa questão, mas não podemos garantir que as informações possam ser obtidas.

Por fim, precisamos reiterar que não recomendamos ou solicitamos que você use nenhum serviço DAPP de terceiros.

# Parâmetros de rede
Os usuários da comunidade podem usar qualquer carteira compatível com Ethereum para configurar com parâmetros de rede KCC, como [metamask](https://metamask.io/), [myetherwallet](https://www.myetherwallet.com/), [imtoken]( https://token.im/), [TokenPocket](https://www.tokenpocket.pro/) etc.

## Rede principal
```
Nome da cadeia: KCC-MAINNET
ID da cadeia: 321
Símbolo: KCS
URL RPC: https://rpc-mainnet.kcc.network
URL do explorador: https://explorer.kcc.io/en
URL de RPC do WebSocket: wss://rpc-ws-mainnet.kcc.network
```

*O limite de taxa do endpoint na Testnet e Mainnet é 300/10s*

*Os usuários também podem usar [https://scan.kcc.io](https://scan.kcc.io) como Block Explorer.*

## Rede de teste
```
Nome da cadeia: KCC-TESTNET
ID da cadeia: 322
Símbolo: KCS
URL RPC: https://rpc-testnet.kcc.network
URL do Explorer: https://scan-testnet.kcc.network
URL de RPC do WebSocket: wss://rpc-ws-testnet.kcc.network

URL da torneira: https://faucet-testnet.kcc.network (apenas para teste, sem valor)
```

# Desenvolvedor

## Nó
### Arquivo binário
Você pode visitar diretamente [https://github.com/kcc-community/kcc/releases](https://github.com/kcc-community/kcc/releases) para baixar a versão mais recente do arquivo binário?

### Docker
Ou você pode visitar [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) para implantação e teste rápidos?([How to use Docker ?](https://docs.docker.com/get-started/))

### Compilação
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
Os sinalizadores de linha de comando são semelhantes ao go-ethereum, você pode usar `./build/bin/geth --help` para todas as opções de linha de comando,
como `./build/bin/geth --testnet` para entrar na Testnet. Cuidado: Use a versão "geth" específica localizada em `./build/bin/geth`.

## Docker

Você pode usar [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) para implantar e testar rapidamente.

[Como usar o Docker?](https://docs.docker.com/get-started/)

## Implantar

### Requisitos
```
CPU de 4 núcleos
8g de memória
SSD de 200G e escalável
IP público com TCP/UDP:30303 aberto
```

#### Comando de partida
```
./geth #Mainnet
./geth --testnet #Testnet

opções úteis:
/data/kcc/get\
--datadir /data/.kcc/testnet \ #seu diretório de dados
--testnet \ #Testnet
--http\#http rpc
--http.addr 0.0.0.0 \ #http rpc endereço de ligação
--http.vhosts * \ #vhosts
--http.corsdomain * \ #http corsdomain
--ws \ #ws rpc
--ws.addr 0.0.0.0 \ #ws rpc endereço de ligação
--syncmode completo \ #syncmode
--gcmode arquivo #gcmode
```

Você pode usar `nohup`,`supervisor`,`systemd` para executar e gerenciar `geth` em segundo plano.

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDK
Você pode usar os seguintes SDKs para interagir com o rpc do nó KCC.

- [Js: web3.js](https://github.com/ChainSafe/web3.js) API JavaScript Ethereum
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
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
KCC introduz um mecanismo de consenso PoSA, que apresenta baixos custos de transação, baixo atraso de transação,
alta simultaneidade de transações e suporta até 29 validadores.

PoSA é uma combinação de PoA e PoS. Para se tornar um validador, você precisa primeiro enviar uma proposta e esperar que outros validadores ativos votem nela. Após mais da metade deles votarem, você estará apto a se tornar um validador. Qualquer endereço pode apostar em um endereço que se qualifique para se tornar um validador e, depois que o volume de staking do validador estiver entre os 29 primeiros, ele se tornará um validador ativo na próxima época.

Todos os validadores ativos são ordenados de acordo com regras predefinidas e se revezam nos blocos de minas. Se um validador falhar em minerar um bloco a tempo durante sua própria rodada, os validadores ativos que não estiveram envolvidos nos últimos n/2 blocos (n é o número de validadores ativos) realizarão o bloqueio aleatoriamente. Pelo menos n/2+1 validadores ativos funcionam corretamente para garantir o bom funcionamento do blockchain.

O valor de dificuldade de um bloco é 2 quando o bloco é gerado normalmente e 1 quando o bloco não é gerado em uma ordem pré-definida. Quando ocorre um fork do blockchain, o blockchain seleciona o fork correspondente de acordo com a dificuldade máxima acumulada.

### Contratos do Sistema
A KCC fez 3 contratos integrados para PoSA no arquivo genesis.

O código-fonte desses contratos é bifurcado do Heco, você pode localizá-los aqui: [https://github.com/kcc-community/kcc-genesis-contracts](https://github.com/kcc-community/kcc -genesis-contratos)?

A gestão dos validadores atuais é toda feita pelos contratos do sistema.

- Proposta Responsável por gerenciar o acesso aos validadores e gerenciar as propostas e votos dos validadores.
- Validadores Responsável pela gestão do ranking de validadores, operações de staking e untaking, distribuição de recompensas em bloco, etc.
- Punir Responsável por punir operações contra validadores ativos que não estejam funcionando corretamente.

Contratos do sistema de chamadas Blockchain:

- Ao final de cada bloco, o contrato de Validadores é chamado e as taxas de todas as transações do bloco são distribuídas aos validadores ativos.
- O contrato Punir é chamado para punir o validador quando o validador não estiver funcionando corretamente.
- Ao final de cada época, o contrato de Validadores é chamado para atualizar os validadores ativos, com base no ranking.

### estaca
Você pode chamar o método `stake` no contrato `validator` para apostar para qualquer validador, o valor mínimo de aposta para cada validador é 32KCS.

### desmarcar
Se você quiser `unstake` seu KCS, você precisa chamar o método `unstake` no contrato `validator`,
e aguarde 86.400 blocos (3 dias), então chame o método `withdrawStaking` no contrato `validator` para disponibilizar o valor.

### punir
Sempre que um validador não minerar um bloco como pré-definido, o contrato Punish é automaticamente chamado ao final deste bloco e o validador é contabilizado. Quando a contagem chega a 24, todos os rendimentos do validador são punidos. Quando a contagem atinge 48, o validador é removido da lista de validadores ativos e o validador é desclassificado.

## O gráfico
O Graph Node é um protocolo para criar aplicativos descentralizados (dApps) rapidamente no Ethereum e IPFS usando o GraphQL.

O nó Graph aberto pela equipe de desenvolvimento da comunidade KCC são:
```
https://thegraph.kcc.network/deploy/
https://thegraph.kcc.network/ipfs/
https://thegraph.kcc.network/subgraphs/name/
```

Exemplo:
```
"auth": "autenticação do gráfico https://thegraph.kcc.network/deploy/ your-token"
"create": "graph create your-name --node https://thegraph.kcc.network/deploy/"
"deploy": "graph deploy your-name --ipfs https://thegraph.kcc.network/ipfs/ --node https://thegraph.kcc.network/deploy/"
"explorer": "https://thegraph.kcc.network/subgraphs/name/your-name"
```

**Se precisar usar o serviço, preencha o [formulário de inscrição](https://forms.office.com/r/DQawaDHtnF)**

**Devido a problemas de desempenho, recomendamos que você siga [The Graph the Official document](https://thegraph.com/docs/) e faça a implantação da privatização e implante seu próprio nó.**


# Governança

## Conselhos, questões e discussões

Qualquer conselho, questões e discussão são bem-vindos.

[Deixe um conselho ou um problema](https://github.com/kcc-community/any-advice-issue/issues)

[Iniciar uma discussão](https://github.com/kcc-community/any-advice-issue/discussions)

Se você tiver um problema em um projeto especial, vá para a página "problema" no projeto especial.


## KIP
Propostas de melhoria do KCC

As propostas de melhoria KCC (KIPs) descrevem os padrões para a plataforma KCC, incluindo Chain, DEX e dApps.

O objetivo deste processo é garantir que as mudanças no KCC sejam transparentes e bem governadas.

URL:[https://github.com/kcc-community/KIPs](https://github.com/kcc-community/KIPs)

# PERGUNTAS FREQUENTES
1. Qual é o mecanismo de consenso do KCC?

>KCC adota o mecanismo de consenso PoSA, apresentando baixo custo, alto desempenho e geração de blocos estável, suportando até 29 validadores;
2.Como se tornar um nó validador KCC?

>Para se tornar um validador, você precisa criar um nó e enviar uma proposta, e aguardar a votação de outros validadores ativos. Depois de receber mais da metade dos votos, você é elegível para se tornar um validador. Qualquer endereço pode apostar no endereço que é elegível para se tornar um validador. Depois que o valor apostado do validador estiver entre os 29 primeiros, o validador se tornará ativo na próxima época.

3. O KCC suporta EVM?

>KCC suporta totalmente EVM e é totalmente amigável para desenvolvedores de Ethereum.

4.Qual SDK o KCC usa?

> O KCC é altamente compatível com o Ethereum, então adotamos o SDK do Ethereum, como web3js, web3j, etc.

5.Quero realizar algumas operações e testes na rede de teste KCC. Onde posso obter tokens de teste?

>Você pode visitar nossa torneira testnet: https://faucet-testnet.kcc.network.

6.Como apostar nós de contrato?

>Os usuários podem chamar o método stake do contrato do validador para fazer o stake de qualquer nó. O valor mínimo apostado para cada validador é de 32 KCS.

7.Como desbloquear o valor apostado?

>Se os usuários quiserem recuperar o KCS apostado, eles precisam chamar o método untake do contrato dos validadores para desbloquear o valor apostado. Após a geração de 86.400 blocos (3 dias), chame o método retiroStaking do contrato dos validadores para recuperar o KCS apostado.

8. Ficar preso ao usar o MetaMask (incluindo, mas não limitado a transferência travada ou atrasada, problema de exibição de dados, etc.)

>Use a visualização de expansão do plug-in para exibir em tela cheia, que pode ser mais estável ou escolha "Acelerar" para aumentar o gaslimt e o gasPrice.

9. Como usar a ponte KCC para o serviço de conversão de ativos de cadeia cruzada?

> Você pode consultar nosso tutorial em vídeo: https://www.youtube.com/watch?v=kZdX1V2Tgnc

>Para mais tutoriais, assine nosso canal do Youtube: https://www.youtube.com/channel/UCZhWm40SuAApnLqqq3F9o1w

10. O que acontece se usarmos KCC em vez de ERC20 ao enviar Tether para um endereço que não suporta KCC? Ele se recupera depois de um certo período de tempo?

> Se o endereço de destino for o seu endereço pessoal, a operação é bastante simples. Altere a rede da carteira para KCC e importe seu endereço e seu endereço de contrato KCC-USDT, então você poderá ver o saldo do USDT.

>Se o seu endereço de destino for uma bolsa ou uma carteira centralizada, você precisa entrar em contato com o suporte ao cliente para permitir que eles suportem o KCC ou reembolsá-los para seu endereço original.

> Portanto, sugerimos que nossos usuários sejam claros sobre o motivo pelo qual farão a transferência, já que o blockchain possui imutabilidade, o que significa que qualquer transferência não pode ser revertida uma vez enviada, e sempre recomendamos primeiro tentar com uma quantidade menor.


## Como configurar a carteira MetaMask

Use o navegador Chrome para abrir o MetaMask [site de extensão](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

Siga a introdução, crie sua carteira ETH,**faça backup de sua chave privada ou mnemônico**;

Configurar rede principal KCC

(1) Abra o MetaMask,você pode ver a configuração padrão da?Ethereum mainnet?

<img width="170" alt="E1" src="https://user-images.githubusercontent.com/13411690/121641021-3f093900-cac1-11eb-9c06-fd653cd598a1.png">


clique em?Ethereum mainnet?,clique em?Custom RPC?no menu suspenso

<img width="170" alt="E2" src="https://user-images.githubusercontent.com/13411690/121641049-4597b080-cac1-11eb-8674-3755c30a3398.png">


(2) Preencha esse valor de configuração para mudar para o KCC Mainnet:

    Nome da rede: KCC-MAINNET
    
    Nova URL RPC: https://rpc-mainnet.kcc.network
    
    ID da cadeia: 321
    
    Símbolo de moeda (opcional): KCS
    
    URL do Explorador de Blocos (opcional): https://explorer.kcc.io/en

<img width="170" alt="E3" src="https://user-images.githubusercontent.com/13411690/121641889-598fe200-cac2-11eb-92c5-6617c103ebee.png">




Feito

<img width="170" alt="E4" src="https://user-images.githubusercontent.com/13411690/121641085-51837280-cac1-11eb-80cd-1a208c0bcd54.png">

## Como desbloquear transações travadas no MetaMask?
[[Vídeo]Como desbloquear transações bloqueadas no MetaMask (KCC)](https://youtu.be/0xkkRmajIJI)

## Como adicionar um token personalizado à sua carteira MetaMask?
[[Vídeo]Como adicionar um token personalizado à sua carteira MetaMask (KCC)](https://youtu.be/tb7xSLur6EU)


