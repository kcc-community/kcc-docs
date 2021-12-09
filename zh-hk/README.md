# KCC

## 社區鏈簡介
KCC是由KCS和KuCoin的社區粉絲構建的，基於以太坊源代碼開發的，高性能和去中心化的公鏈，**目的是為了解決當前公鏈出現的性能底下，成本過高等問題，從而為社區用戶提供更快速的體驗能力，可以使用區塊鏈使用**。

KCC具有如下特性：
- 完全兼容以太坊和ERC20智能合約，遷移成本極低
- 以KCS作為鏈的gas費，交易成本極低
- 每3秒出一個塊，交易確認更快，鏈性能提高
- PoSA 授權算法，效率高，安全穩定

## 使命

促進價值在全球流通流通

## 風險提示

- KCC官方不會發布任何Swap項目，因為所有項目都是由社區開發的，所以KCC對這些項目造成的問題不承擔任何責任。此外，KCC不為相關項目提供客戶服務；
- 在任何加密貨幣，Defi相關領域有任何操作前，請先DYOR（Do your own research）；
- 所有用戶及開發者都可以免費參與KCC的測試環境與後續階段，不存在收費場景；
- 大家務必區分好測試環境和主網環境，測試環境所產生的資產不具備任何價值，謹防假幣詐騙；
- KCC將通過官方社交平台發布授權、推介等合作，開發者和用戶謹慎核對，以免引發損失；
- 請認准官方網址，避免出現私鑰被釣魚等情況。

## 免責聲明
尊敬的用戶（以下稱“您”）：

KCC（以下簡稱“KCC”或“我們”）是一個去中心化公鏈，全球開發者都可以在KCC上部署應用，所有用戶可以在KCC上可以讀取、發送和交易。由於去中心化的特性，我們特向您提醒第三方DAPP風險如下：
- 您在任何平台、錢包、第三方Dapp有任何操作前，請首先DYOR(Do your own research)；
- 無論您通過任何交易平台、錢包參與或使用KCC上的DAPP，均為您個人的自由選擇行為，我們並不向您推薦使用；
- 我們不對任何第三方DAPP負有審核責任，也不對其服務所涉及的技術及信息的有效性、準確性、正確性、可靠性、質量、穩定、完整和及時性作出任何承諾和保證；
- 您自行承擔使用第三方DAPP服務產生的全部責任；
- 第三方DAPP服務等是否符合您所在管轄區的法律法規或相關政策要求，請您自行判斷與評估，我們不提供任何評估意見，但請您務必嚴格遵守您所在管轄地的法律；
- 您因使用第三方DAPP而涉及的包括但不限於合法問題、合同責任問題、經濟損失問題等，均由您與第三方DAPP自行解決，我們不對此承擔責任；
- KCC不會與任何第三方DAPP共享您的個人信息，除非獲得您的明確同意。在獲得您明確同意後而因第三方DAPP 獲取您個人信息產生的一切法律責任、糾紛，仍由您自行承擔並與第三方DAPP自行解決。
- KCC無權向您提供任何第三方DAPP開發者的個人信息，除非獲得對方的同意或相關部門的要求，我們會盡力協助但無法保證能有效及時獲取對方信息。
  最後，我們再次提醒您：我們不推薦、建議、引導您使用任何第三方DAPP服務。

# 網絡參數
社區用戶可以使用任何以太坊的錢包，並配置KCC鏈的網絡參數，如 [metamask](https://metamask.io/), [myetherwallet](https://www.myetherwallet.com/), [imtoken](https://token.im/), [TokenPocket](https://www.tokenpocket.pro/) 等。

## 主網
```
網絡名稱: KCC-MAINNET
鏈ID: 321
符號: KCS
RPC地址: https://rpc-mainnet.kcc.network
瀏覽器地址: https://explorer.kcc.io/cn
WebSocket RPC地址: wss://rpc-ws-mainnet.kcc.network
```

## 測試網
```
網絡名稱: KCC-TESTNET
鏈ID: 322
符號: KCS
RPC地址: https://rpc-testnet.kcc.network
瀏覽器地址: https://scan-testnet.kcc.network
WebSocket RPC地址: wss://rpc-ws-testnet.kcc.network

水龍頭: https://faucet-testnet.kcc.network (僅測試用，無價值)
```
# 開發者

## 運行節點
### 二進製文件
直接訪問[https://github.com/kcc-community/kcc/releases](https://github.com/kcc-community/kcc/releases)下載最新版本的二進製文件。

### Docker
也可以使用 [https://hub.docker.com/r/kucoincommunitychain/kcc](https://hub.docker.com/r/kucoincommunitychain/kcc) 進行快速部署和測試。 ([關於如何使用Docker？](https://docs.docker.com/get-started/))

### 編譯
#### 編譯要求
- Linux or Mac
- golang >= 1.13
- git

golang安裝和配置請參考 [https://golang.org/doc/install](https://golang.org/doc/install)

#### 編譯步驟
```
git clone -b kcc --single-branch https://github.com/kcc-community/kcc.git
cd kcc
make geth
```
#### 啟動
啟動參數配置和以太坊類似，可以通過`./build/bin/geth --help`查看所有的參數配置，可以通過`geth --testnet`加入測試網。

### 部署

#### 推薦配置
```
4核
8G內存
200G並且可擴容的SSD
公網IP並開啟TCP/UDP:30303端口
```

#### 啟動命令
```
./geth #主網
./geth --testnet #測試網

部分常用參數示例：
/data/kcc/geth \
--datadir /data/.kcc/testnet \ #自定義數據目錄
--testnet \ #測試網
--http \ #開啟http rpc
--http.addr 0.0.0.0 \ #http rpc監聽地址
--http.vhosts * \ #vhosts
--http.corsdomain * \ #http corsdomain
--ws \ #開啟ws rpc
--ws.addr 0.0.0.0 \ #ws rpc監聽地址
--syncmode full \ #同步模式
--gcmode archive #gc模式
```

可以使用`nohup`,`supervisor`,`systemd`等，使`geth`在後台常駐運行。

參考文檔：

- [supervisor](http://supervisord.org/)
- [systemd](https://wiki.debian.org/systemd)

## SDKs

可以使用以下的SDK和KCC的RPC API進行交互。

- [Js: web3.js](https://github.com/ChainSafe/web3.js) Ethereum JavaScript API
- [Java: web3j](https://github.com/web3j/web3j) Web3 Java Ethereum Ðapp API
- [PHP: web3.php](https://github.com/sc0Vu/web3.php) A php interface for interacting with the Ethereum blockchain and ecosystem.
- [Python: Web3.py](https://github.com/ethereum/web3.py) A Python library for interacting with Ethereum, inspired by web3.js.
- [Golang: go-ethereum](https://github.com/ethereum/go-ethereum)

## 工具
- [合約開發語言：solidity](https://docs.soliditylang.org/en/latest/)
- [合約開發工具：remix](https://remix.ethereum.org/)
- [合約開發套件: truffle](https://www.trufflesuite.com/docs/truffle/overview)
- [合約開發套件: hardhat](https://hardhat.org/)
- [水龍頭: faucet](https://faucet-testnet.kcc.network)
- [瀏覽器: explorer](https://explorer.kcc.io)

## 跨鏈橋
- [KCC-Bridge](https://www.kcc.io/bridge/transfer/)
- [AnySwap](https://anyswap.exchange/bridge)

## 共識
KCC採用PoSA共識機制，具有成本低、性能高、出塊穩的特點，支持最多29個驗證人節點；

PoSA結合了PoS和PoA，想要成為驗證人，需要先創建節點並提交提案，等待其他活躍的驗證人進行投票，半數以上通過之後，則有資格成為驗證人。任意地址均可對有資格成為驗證人的地址進行質押，當驗證人的質押量排名進入前29位之後，則會在下一個epoch成為活躍驗證人。

所有的活躍驗證人按照預定規則排序，輪流進行出塊。如果有驗證人在自己的出塊輪次沒能及時出塊，則在過去n/2(n為活躍驗證人的數量)個塊內，沒有參與過出塊操作的活躍驗證人，隨機進行出塊。最少n/2+1個活躍驗證人正常工作，即可保證區塊鏈的正常運行。

正常產塊時，區塊的難度值為2，未按照預定順序進行產塊時，區塊的難度值為1。當區塊鏈發生分叉時，區塊鏈按照累計最大難度選擇對應分叉。

### 內置合約
KCC在genesis文件中內置了PoSA共識相關的合約，
合約源代碼fork自heco，可在[https://github.com/kcc-community/kcc-genesis-contracts](https://github.com/kcc-community/kcc-genesis-contracts)查看。

目前驗證人的管理，均由系統合約完成，目前的系統合約有：
- proposal 負責管理驗證人的准入資格，管理驗證人提案和投票；
- validators 負責對驗證人進行排名管理、質押和解質押操作、分發區塊獎勵等；
- punish 負責對不正常工作的活躍驗證人進行懲罰操作；

區塊鏈調用系統合約：
- 每個塊結束的時候，會調用validators合約，將區塊中所有交易的手續費分發給active validator;
- 發現validator沒有正常工作的時候，會調用punish合約，對validator進行懲罰；
- 每個epoch結束的時候，會調用validators合約，根據排名，更新active validator；

### 質押
用戶可以調用validator合約的`stake`方法，對任意節點進行質押，每個validator的最小質押量是32KCS。

### 解質押
如果用戶想取回質押的KCS，需要先調用validators合約的`unstake`方法進行解質押，然後在86400個塊之後(3天)，再調用validators合約的`withdrawStaking`方法才能把質押的KCS取回到可用餘額。

### 懲罰
如果驗證人沒有按照預定規則進行出塊，就會在這個塊結束時，自動調用punish合約，對驗證人進行計數。當計數達到24次時，罰沒驗證人的所有收入。當計數達到48次時，將驗證人移除出活躍驗證人列表，同時取消驗證人資格。

# 社區治理

## 建議&問題&討論

我們歡迎社區的任何建議、問題和討論，並建立了通用的Github渠道：

[建議和問題](https://github.com/kcc-community/any-advice-issue/issues)

[討論](https://github.com/kcc-community/any-advice-issue/discussions)

關於某一個具體項目的問題，請移步到具體的項目中開啟`issue`。


## KIPs
KCC Improvement Proposals

KIP是KCC改進提議的縮寫，任何社區用戶都可以在這裡發起有關KCC及相關應用的提議，
參與討論並執行。

提議地址：[https://github.com/kcc-community/KIPs](https://github.com/kcc-community/KIPs)

# FAQ
1.KCC的共識機制是什麼？

>KCC採用PoSA共識機制，具有成本低、性能高、出塊穩的特點，支持最多29個驗證人節點；

2.如何成為KCC驗證人節點

>想要成為驗證人，需要先創建節點並提交提案，等待其他活躍的驗證人進行投票，半數以上通過之後，則有資格成為驗證人。任意地址均可對有資格成為驗證人的地址進行質押，當驗證人的質押量排名進入前29位之後，則會在下一個epoch成為活躍驗證人。

3.KCC是否支持EVM？

>KCC完全支持以太坊EVM，對以太坊開發者完全友好。

4.KCC使用什麼sdk?

>KCC高度兼容 Ethereum，因此使用 Ethereum 的 sdk，例如 web3js， web3j 等。

5.我想在KCC測試網進行一些操作與測試，去哪可以獲得測試代幣？

>可以訪問我們的測試網水龍頭：https://faucet-testnet.kcc.network.

6.如何對合約節點進行質押？

>用戶可以調用validator合約的stake方法，對任意節點進行質押，每個validator的最小質押量是32KCS。

7.如何進行解質押？

>如果用戶想取回質押的KCS，需要先調用validators合約的unstake方法進行解質押，然後在86400個塊之後(3天)，再調用validators合約的withdrawStaking方法才能把質押的KCS取回到可用餘額。

8.使用METAMASK卡頓（包括但不限於轉賬卡頓、延遲，數據顯示等問題）

>使用插件的 expand view（擴展視圖）模式全屏展示更穩定；
>選擇“加速”，將gaslimt和gasPrice調高。

9.如何使用KCC Bridge進行資產跨鏈？

>可以參考我們的視頻教程：https://www.youtube.com/watch?v=kZdX1V2Tgnc

>更多教程歡迎訂閱我們的Youtube頻道：https://www.youtube.com/channel/UCZhWm40SuAApnLqqq3F9o1w

10.如果我們將Tether發送到不支持KCC的地址時使用的是ERC20而不是KCC會發生什麼？代幣會在一段時間後返還到原錢包地址嗎？

>如果目標地址是您的個人地址，則操作非常簡單。把錢包網絡改成KCC，導入你的地址和你的KCC-USDT合約地址，就可以看到USDT餘額了。

>如果您的目標地址是交易所或中心化錢包，您需要聯繫他們的客戶支持，讓他們支持 KCC 或將其退款到您的原始地址。

>因此，我們建議我們的用戶清楚他們為什麼要進行代幣轉移，因為區塊鏈具有不可變性，這意味著任何轉移一旦發送就無法回滾，所以我們建議您先用較小的金額進行嘗試。

## 如何配置 MetaMask 錢包

使用 Chrome 瀏覽器打開 MetaMask [安裝地址](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=zh-CN)

根據頁面提示創建以太坊錢包，**備份好私鑰及助記詞**；

切換到 KCC 主網

(1) 打開 MetaMask，可以看到錢包被默認設置成【以太坊主網】。

<img width="170" alt="C1" src="https://user-images.githubusercontent.com/13411690/121639732-8e4e6a00-cabf-11eb-8c81-a7ac380bd2b9.png">



點擊【以太坊主網】，在下拉菜單中點擊【自定義 RPC】


<img width="170" alt="C2" src="https://user-images.githubusercontent.com/13411690/121639736-90b0c400-cabf-11eb-93ab-794d99bf28d9.png">



(2) 切換到 KCC 主網請在表單中填入下列數據：

    網絡名稱：KCC-MAINNET
    
    RPC URL：https://rpc-mainnet.kcc.network
    
    ChainID: 321
    
    符號：KCS
    
    瀏覽器鏈接:https://explorer.kcc.io/cn

<img width="170" alt="C3" src="https://user-images.githubusercontent.com/13411690/121639766-9e664980-cabf-11eb-9b5d-0060c9d05e9b.png">


成功

<img width="170" alt="C4" src="https://user-images.githubusercontent.com/13411690/121639786-a6be8480-cabf-11eb-9ff0-76995dfdccfa.png">

## 如何處理MetaMask卡住的交易？
[[視頻]How to Unstuck Stuck Transactions on MetaMask (KCC)](https://youtu.be/0xkkRmajIJI)

## 如何在MetaMask添加KCC上的資產?
[[視頻]How to add a custom token to your MetaMask wallet (KCC)](https://youtu.be/tb7xSLur6EU)



