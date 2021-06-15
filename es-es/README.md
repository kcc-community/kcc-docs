# KuCoin Community Chain

## Introducción
KuCoin Community Chain (KCC) es una cadena pública descentralizada y de alto rendimiento construida por fanáticos de KCS y KuCoin.

Desarrollado en base a go-ethereum con el propósito de proporcionar a los usuarios de la comunidad una mayor velocidad,
experiencia de usuario de blockchain conveniente y de bajo costo.

KuCoin Community Chain (KCC) tendrá las siguientes características:
- Totalmente compatible con contratos inteligentes Ethereum y ERC-20, con costos de migración extremadamente bajos;
- KuCoin Token (KCS) servirá como el único combustible central y token nativo para KCC y se puede utilizar en escenarios como el pago de tarifas de gas;
- Un bloque cada 3 segundos da como resultado una confirmación de transacción más rápida y un mayor rendimiento de la cadena;
- Algoritmo de consenso Proof of Staked Authority (PoSA), alta eficiencia, seguridad y estabilidad.

## Misión

Misión: Acelerar el flujo de valor en todo el mundo sin fronteras.

## Declaración de riesgo

- Antes de cualquier operación en los campos relacionados con la criptomoneda o DeFi, primero haga su propia investigación.
- Todos los usuarios y desarrolladores pueden construir la dApp en KCC testnet y luego en la mainnet de forma gratuita.
- Distinga el entorno de prueba (testnet) del entorno de red principal (mainnet). Los activos generados en el entorno de prueba no tienen valor, así que tenga cuidado con el fraude de criptomonedas.
- KCC anunciará la autorización, promoción y otra cooperación a través de su red social oficial, por favor verifique la información oficial y evite los sitios de phishing.
- Asegúrese de visitar el sitio web oficial para evitar la pérdida de la clave privada.

## Descargos de responsabilidad
Estimado usuario (en lo sucesivo, "usted"):

KuCoin Community Chain (en lo sucesivo, "KCC" o "nosotros") es una cadena pública descentralizada. Los desarrolladores de todo el mundo pueden implementar aplicaciones en KCC, todos los usuarios pueden leer, enviar e intercambiar en KCC. Debido a las características de la descentralización, le recordamos que los riesgos de las DAPP de terceros son los siguientes:

- Antes de operar en cualquier plataforma, billetera o DAPP de terceros, primero haga su propia investigación;
- Ya sea que participe o use DAPP en KCC a través de cualquier plataforma de negociación o billetera, es su propio comportamiento y no se lo recomendamos;
- No somos responsables de auditar ningún DAPP de terceros, ni asumimos ningún compromiso y garantía sobre la validez, exactitud, corrección, confiabilidad, calidad, estabilidad, integridad y oportunidad de la tecnología e información involucrada en sus servicios;
- Debe asumir todas las responsabilidades derivadas de su uso de cualquier servicio de DAPP de terceros por su cuenta;
- Ya sea que los servicios de DAPP de terceros cumplan con las leyes, regulaciones o políticas relevantes de su jurisdicción, haga su propio juicio y evaluación. No proporcionamos ninguna evaluación, asegúrese de cumplir estrictamente con las leyes de su jurisdicción;
- Usted y el DAPP de terceros asumirán las responsabilidades de cualquier problema relacionado con el uso del DAPP de terceros, incluidos, entre otros, problemas legales, problemas de responsabilidad contractual, pérdidas económicas, etc., KCC no será responsable de ellos;
- A menos que nos autorice a hacerlo, KCC no compartirá su información personal con ningún DAPP de terceros. Si nos autoriza a compartir la información, todas las responsabilidades legales y disputas que surjan del acceso del tercero DAPP a su información personal serán asumidas por usted y la DAPP de terceros.
- KCC no tiene derecho a proporcionarle la información personal de ningún desarrollador de DAPP de terceros a menos que estén de acuerdo en hacerlo. Ayudaremos en este problema, sin embargo, no podemos garantizar que se pueda obtener la información.

Finalmente, debemos reiterar que no recomendamos ni le pedimos que utilice ningún servicio DAPP de terceros.

# Parámetros de red
Los usuarios de la comunidad pueden usar cualquier billetera compatible con Ethereum para configurar con parámetros de red KCC, como [metamask](https://metamask.io/), [myetherwallet](https://www.myetherwallet.com/), [imtoken](https://token.im/), [TokenPocket](https://www.tokenpocket.pro/) etc.

## Mainnet
```
Chain Name: KCC-MAINNET
Chain ID: 321
Symbol: KCS
RPC URL: https://rpc-mainnet.kcc.network
Explorer URL: https://explorer.kcc.io/en
WebSocket RPC URL: wss://rpc-ws-mainnet.kcc.network
```

## Testnet
```
Chain Name: KCC-TESTNET
Chain ID: 322
Symbol: KCS
RPC URL: https://rpc-testnet.kcc.network
Explorer URL: https://scan-testnet.kcc.network
WebSocket RPC URL: wss://rpc-ws-testnet.kcc.network

Faucet URL: https://faucet-testnet.kcc.network (for test only, no value)
```

# Documentación para desarrolladores

## Compilacion
### Requisitos
- Linux o Mac
- golang >= 1.13
- git

[cómo descargar e instalar golang](https://golang.org/doc/install)

### Pasos
```
git clone -b kcc --single-branch https://github.com/kucoin-community-chain/kcc.git
cd kcc
make geth
```
### Ejecutando
Los parametros de la línea de comando son similares a go-ethereum, puede usar `./build/bin/geth --help` para todas las opciones de la línea de comandos,
como `./build/bin/geth --testnet` para unirse a Testnet. Precaución: utilice la versión "geth" específica que se encuentra en `./build/bin/geth`.

## Docker

Puedes usar [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) para implementar y probar rápidamente.

[¿Cómo utilizar Docker?](https://docs.docker.com/get-started/)

## Despliegue

### Requisitos
```
4 core cpu
8g memory
scalable SSD disk
public ip with TCP/UDP:30303 open
```

### Comando de Inicio
```
./build/bin/geth #Mainnet
./build/bin/geth --testnet #Testnet

useful options:
/data/kcc/geth \
--datadir /data/.kcc/testnet \ #your data dir
--testnet \ #Testnet
--http \ #http rpc
--ws \ #ws rpc
--http.vhosts '*' \ #vhosts
--rpccorsdomain '*' \ #http corsdomain
--http.addr 0.0.0.0 \ #http rpc bind address
--ws.addr 0.0.0.0 \ #ws rpc bind address
--syncmode full \ #syncmode
--gcmode archive #gcmode
```

Puedes usar `nohup`,`supervisor`,`systemd` para ejecutar y administrar `geth` en segundo plano.

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDKs
Puede utilizar los siguientes SDK para interactuar con el nodo rpc de KCC.

- [Js: web3.js](https://github.com/kucoin-community-chain/web3.js) Ethereum JavaScript API
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) A php interface for interacting with the Ethereum blockchain and ecosystem.
- [Python: Web3.py](https://github.com/ethereum/web3.py) A Python library for interacting with Ethereum, inspired by web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## Consenso
KCC presenta un mecanismo de consenso PoSA, que presenta bajos costos de transacción, bajo retraso en la transacción, alta concurrencia de transacciones y admite hasta 29 validadores.

PoSA es una combinación de PoA y PoS. Para convertirse en un validador, primero debe enviar una propuesta y esperar a que otros validadores activos la voten. Después de que más de la mitad de ellos hayan votado, será elegible para convertirse en validador. Cualquier dirección puede hace stake a una dirección que califique para convertirse en un validador, y después de que el volumen de stake del validador se ubique entre los 29 primeros, se convertirá en un validador activo en la próxima época.

Todos los validadores activos se ordenan de acuerdo con reglas predefinidas y se turnan para extraer bloques. Si un validador no puede extraer un bloque a tiempo durante su propia ronda, los validadores activos que no han estado involucrados en el pasado n / 2 (n es el número de validadores activos) bloques realizarán el bloqueo al azar. Al menos n / 2 + 1 validadores activos funcionan correctamente para garantizar el correcto funcionamiento de la cadena de bloques.

El valor de dificultad de un bloque es 2 cuando el bloque se genera normalmente y 1 cuando el bloque no se genera en un orden predefinido. Cuando se produce una bifurcación de la cadena de bloques, la cadena de bloques selecciona la bifurcación correspondiente de acuerdo con la dificultad máxima acumulada.

### Contratos de Sistema
KCC ha realizado 3 contratos integrados para PoSA en el archivo de génesis.

El código fuente de esos contratos se bifurcaron desde Heco, puede ubicarlos aquí: [https://github.com/kucoin-community-chain/kcc-genesis-contracts](https://github.com/kucoin-community-chain/kcc-genesis-contracts)。

La gestión de los validadores actuales se realiza mediante los contratos del sistema.

- Responsable de Propuesta Responsable de gestionar el acceso a los validadores y gestionar las propuestas y votaciones de los validadores.
- Responsables de validadores de la gestión de ranking de validadores, operaciones de staking y unstaking, distribución de recompensas en bloque, etc.
- Responsable de Sanciones de sancionar operaciones contra validadores activos que no estén funcionando correctamente.

Contratos del sistema de llamadas blockchain:

- Al final de cada bloque, se llama al contrato de Validadores y las tarifas de todas las transacciones en el bloque se distribuyen a los validadores activos.
- El contrato Sanciones está llamado a castigar al validador cuando el validador no está funcionando correctamente.
- Al final de cada época, se llama al contrato de Validadores para actualizar los validadores activos, en función del ranking.

### stake
Puede llamar al método de stake en el contrato del validador para hacer stake por cualquier validador, la cantidad mínima de stake para cada validador es 32KCS.

### unstake
Si desea hacer "unstake" de sus KCS, debe llamar al método "unstake" en el contrato del "validador",
y esperar 86400 bloques (3 días), luego llame al método `withdrawStaking` en el contrato del `validador` para que la cantidad esté disponible.

### Sanción
Siempre que se encuentra que un validador no extrae un bloque como estaba predefinido, el contrato de Sanción se llama automáticamente al final de este bloque y se cuenta el validador. Cuando el recuento llega a 24, se castigan todos los ingresos del validador. Cuando el recuento llega a 48, el validador se elimina de la lista de validadores activos y el validador queda descalificado.

# Governanza

## Asesoramiento, problemas y debates

Cualquier consejo, problema y discusión son bienvenidos.

[Deja un consejo o un problema](https://github.com/kucoin-community-chain/any-advice-issue/issues)

[Iniciar una discusión](https://github.com/kucoin-community-chain/any-advice-issue/discussions)

Si tiene un problema en un proyecto especial, vaya a la página "problema" del proyecto especial.


## KIPs
Propuestas de mejora de KCC

Las propuestas de mejora de KCC (KIP) describen los estándares para la plataforma KCC, incluidos Chain, DEX y dApps.

El propósito de este proceso es garantizar que los cambios en KCC sean transparentes y estén bien gobernados.

URL：[https://github.com/kucoin-community-chain/KIPs](https://github.com/kucoin-community-chain/KIPs)

# FAQ
1. ¿Cuál es el mecanismo de consenso de KCC?

> KCC adopta el mecanismo de consenso PoSA, con bajo costo, alto rendimiento y generación de bloques estable, que admite hasta 29 nodos de validación;

2.¿Cómo convertirse en un nodo validador de KCC?

> Para convertirse en un validador, debe crear un nodo y enviar una propuesta, y esperar a que otros validadores activos voten. Después de recibir más de la mitad de los votos, es elegible para convertirse en validador. Cualquier dirección puede hacer stake a la dirección que es elegible para convertirse en validador. Después de que la cantidad apostada del validador se ubique entre los 29 primeros, el validador se convertirá en uno activo en la próxima época.

3. ¿KCC es compatible con EVM?

> KCC es totalmente compatible con EVM y es completamente amigable con los desarrolladores de Ethereum.

4. ¿Qué SDK utiliza KCC?

> KCC es altamente compatible con Ethereum, por lo que adoptamos el sdk de Ethereum como web3js, web3j, etc.

5. Quiero realizar algunas operaciones y pruebas en la testnet de KCC. ¿Dónde puedo conseguir tokens de prueba?

> Puede visitar nuestro grifo de testnet: https://faucet-testnet.kcc.network.

6.¿Cómo hacer stake en los nodos contractuales?

> Los usuarios pueden llamar al método de stake del contrato del validador para hacer stake a cualquier nodo. La cantidad mínima de stake para cada validador es 32 KCS.

7.¿Cómo desbloquear la cantidad de stake?

> Si los usuarios quieren recuperar el KCS en stake, deben llamar al método unstake del contrato de validadores para desbloquear la cantidad de stake. Después de que se generen 86,400 bloques (3 días), llame al método de retiro del contrato de validación para recuperar el KCS en stake.

8. Quedarse atascado al usar MetaMask (que incluye, entre otros, transferencias atascadas o demoras, problemas de visualización de datos, etc.)

> Utilice la vista de expansión del complemento para mostrar en pantalla completa, que puede ser más estable o elija "Acelerar" para aumentar el gaslimit y el gasPrice.

## Cómo configurar MetaMask Wallet

Utilice el navegador Chrome abra MetaMask [extension site](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

Siga la introducción, cree su billetera ETH, ** aga una copia de seguridad de su clave privada o mnemotécnica** ；

Configure KCC Mainnet

(1) Abra MetaMask, puede ver la configuración predeterminada de 【Ethereum mainnet】。

<img width="170" alt="E1" src="https://user-images.githubusercontent.com/13411690/121641021-3f093900-cac1-11eb-9c06-fd653cd598a1.png">


haga clic en 【Ethereum mainnet】, haga clic en 【RPC personalizado】 en el menú desplegable

<img width="170" alt="E2" src="https://user-images.githubusercontent.com/13411690/121641049-4597b080-cac1-11eb-8674-3755c30a3398.png">


(2) Complete ese valor de configuración para cambiar a la red de KCC:

    Network Name：KCC-MAINNET
    
    New RPC URL：https://rpc-mainnet.kcc.network
    
    Chain ID: 321
    
    Currency Symbol (optional)：KCS
    
    Block Explorer URL (optional):https://explorer.kcc.io/en

<img width="170" alt="E3" src="https://user-images.githubusercontent.com/13411690/121641889-598fe200-cac2-11eb-92c5-6617c103ebee.png">




Hecho

<img width="170" alt="E4" src="https://user-images.githubusercontent.com/13411690/121641085-51837280-cac1-11eb-80cd-1a208c0bcd54.png">
