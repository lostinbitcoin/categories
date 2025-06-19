---
title: ニュートリノ
taxonomy:
    category:
        - glossary
---

## Neutrino
2,100 sats

ニュートリノは[軽量クライアント](https://lostinbitcoin.sakuraweb.com/glossary/light_client/)用[プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)で、既存の軽量クライアント設計、特に簡易支払い検証（SPV）方式に比べて、プライバシーと効率性を向上させることを目的としています。

従来の軽量クライアントは、中央サーバーや[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)ネットワーク内の他のノードから関心のある[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)や[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)に関するデータを要求します。この際リクエストした[アドレス](https://lostinbitcoin.sakuraweb.com/glossary/address/)やトランザクションがサーバーに漏れるため、プライバシーが損なわれるという問題がありました。これを回避するために、これまでにも複数の方式が提案され、さまざまな[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet-2/)で実装されていますが、いまだ標準化された方式はありません。

ニュートリノプロトコルは、軽量クライアントのプライバシーを保護するために、サーバーからブロック内のすべてのトランザクション出力を軽量クライアントに送信します。その後、軽量クライアントが、関心のあるトランザクションが含まれているかを自身で判断します。もし対象となるトランザクションが存在する場合、軽量クライアントはそのトランザクションが含まれるブロック全体を要求し、その中に当該トランザクションが含まれているかを信頼性なしに検証します。この方式はプライバシーを大幅に向上させる一方で、既存の[SPV](https://lostinbitcoin.sakuraweb.com/glossary/spv/)方式に比べて帯域幅と計算負荷を大幅に増加させるというトレードオフの関係にあります。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
