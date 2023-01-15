---
title: 用語集
taxonomy:
    category:
        - glossary
---

### 日本一充実したビットコイン用語集を作りたい！

[River Financial の Bitcoin Glossary](https://river.com/learn/terms/) をベースに、日本語のビットコイン用語集を構築中です。用語集作りに参加して、**ビットコイン**を稼ぎませんか？

以下の英語の用語説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。<br>
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

--
### ビットコイン用語集
#### 索引　[あ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#a)　[か](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ka/#ka)　[さ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#sa)　[た](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#ta)　[な](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-na/#na)　[は](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#ha)　[ま](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ma/#ma)　[や](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ya/#ya)　[ら](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ra/#ra)　</a>[わ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-wa/#wa)　[英数字](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-number/#number)
--

### <a id="ra"></a>ら

|  用語<br>英語表記<br>報酬  |  説明  |
| ---- | ---- |
|ライトニング・インボイス<br>Lightning Invoice<br>2,100 sats | <a id="lightning_invoice"></a>ライトニング・インボイスは一般的な請求書と同様で支払依頼の役割を果たします。ライトニング・インボイスには支払金額、支払先、メタデータ、およびメッセージなどが含まれ、たいていQRコードの形で表現されます。支払人は受取人が作ったQRコードを読み取るだけでライトニング・ネットワーク上での支払いを円滑に行うことができます。|
|ライトニング実装<br>Lightning Implementations<br>2,100 sats | <a id="lightning_implementations"></a>ライトニング実装とはライトニングノードを稼働させ、ライトニングネットワークと接続することが可能なソフトウェアプログラムのことです。 <br>ライトニング実装には様々なプログラミング言語で書かれた複数の異なる実装が存在します。<br>最も一般的なライトニング実装は、LND、c-lightning、Electrum Lightning、Eclairなどです。<br>各実装は微妙に異なる機能や設計を提供していますが、すべての実装はBasis of Lightning Technology (BOLT) 仕様で定義された規格に準拠しています。<br>この仕様ではあるライトニング実装が他のすべての実装と相互運用できるように必要な機能を定義しています。 |
|ライトニング・チャネル<br>Lightning Channel<br>2,100 sats |<a id="lightning_channel"></a>A Lightning channel is a connection between two parties, and the Lightning Network is composed of thousands of channels. Lightning transactions are sent back and forth over channels and are used to recalibrate the bitcoin balances of each party in this channel. All bitcoin in a channel belongs to one of the two parties. Lightning channels are called bidirectional payment channels because both parties can send and receive bitcoin across the channel. In order to open a Lightning channel, two parties, say Alice and Bob, cooperatively construct a 2-of-2 multisig address. Any bitcoin sent to this address requires two signatures, one from each party, in order to be spent. Imagine Alice and Bob open a channel and deposit 1 BTC each. If Alice now wishes to pay Bob 0.5 BTC, she signs a transaction spending from the multisig address. This transaction has two outputs: Bob will receive 1.5 BTC and Alice will receive 0.5 BTC. Since spending from the multisig address requires two signatures, this is not yet a valid transaction, and Alice cannot broadcast it to the Bitcoin network. Instead, she sends the partially-signed transaction, called a commitment transaction, to Bob, who keeps it but does not broadcast it. Alice has paid Bob 0.5 BTC, but Bob has not settled this payment to the Bitcoin blockchain. This is why Lightning transactions are so cheap: they do not require miners to confirm each transaction in a block. A Lightning channel can be closed at any point by publishing the latest unbroadcast commitment transaction. This transaction will send the bitcoin from multisig address to each party in the correct amount, representing the net flow of bitcoin across all of the Lightning transactions that occured on this channel. |
|ライトニング・ネットワーク<br>Lightning Network<br>2,100 sats |<a id="lightning_network"></a>ライトニング・ネットワーク（Lightning Network 略称LN）はビットコインを即時かつ安価に送金できるように設計されたプロトコルです。ライトニング・ネットワークはまだ実験的な段階にありますが、ビットコインのトランザクション処理能力を増強することが期待できます。このプロトコルは双方向のペイメントチャネルを中心に構築されており、2者間の相互送金を可能にします。また、ペイメントチャネルで直接接続されていない2者間でも、複数チャネルを中継することで相互に送金できます。<br>双方向ペイメントチャネルの開設には、オンチェーン上で2者で作ったマルチシグアドレスへビットコインを送ることが必要です。マルチシグアドレスのビットコインは、ライトニング・ネットワーク上で使う限り、オンチェーン上でのビットコインの移動を伴わず（ブロックチェーンにトランザクションを記録せず）、2者間で瞬時かつ無料で送金できます。<br>例えば、アリスとボブがそれぞれ0.5BTCずつ合計1BTCをマルチシグアドレスへ拠出した場合、ライトニング・ネットワーク上の2人の残高はそれぞれ0.5BTCとなります。この際、インプットがマルチシグアドレスの1BTC、アウトプットがアリスに0.5BTC、ボブに0.5BTCというトランザクションが作成されます。アリスがボブに0.1BTCを送ると、トランザクションはインプットはそのままで、アウトプットがアリス0.4BTC、ボブ0.6BTCに更新されますが、まだビットコインネットワークに送信されません。アリスとボブは必要に応じて送金を続け、何度でもトランザクションを更新できます。2人がペイメントチャネルを閉じる時に初めて、最後に更新した最新トランザクションがビットコインネットワークに送信されます。このトランザクションによって、アリスとボブのライトニング・ネットワーク上での残高がそれぞれのウォレットへ送金されます。 |
|レイヤー<br>Layer<br>2,100 sats | <a id="layer"></a>Bitcoin’s blockchain offers final settlement for bitcoin at the cost of relatively low throughput. The Bitcoin network averages between 4-7 transactions per second. This is obviously insufficient for hosting all of the world’s financial transactions, as Bitcoin intends to do. While larger settlements can still be settled to the blockchain to achieve maximal security, smaller transactions in need of lower security can be executed “off-chain” by another service or protocol, called a layer. Layered solutions can trade lower security for higher throughput and cheaper fees. Bitcoin developers prefer that innovation and scaling takes place on layers on top of Bitcoin in order to separate the security risks that come with software innovation from affecting Bitcoin’s blockchain. These layers have analog examples in the legacy financial system: credit cards, Venmo, and PayPal are all layered on top of a core banking system of wire transfers and the ACH system. Before the gold standard was abandoned, physical cash was a layer on top of the base money of gold.|

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
