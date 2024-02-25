---
title: LNURL
taxonomy:
    category:
        - glossary
---

## LNURL
2,100 sats

LNURLは、QRコードを通じてライトニング[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)（以下、LNウォレット）と他のアプリケーションとの通信をより容易にします。LNURLは、取引先との完全な長さの[ライトニング・インボイス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_invoice/)（以下、LNインボイス）の交換など、複雑な支払いフローを抽象化することで、ライトニングでのより良いユーザー体験を実現します。<br>
技術的には、「LNURL」はオープンソースの[プロトコル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/protocol/)の集まりで、HTTPを活用して[ライトニング・ネットワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_network/)上での支払いを調整するために機能します。

ユーザーは、LNURLをサポートするサービスにLNウォレットでログインできるほか、通常はQRコードの形をした静的な支払いコードを利用して支払いを送受信できます。本稿執筆時点で、LNURLにはアプリケーションに実装可能な20の機能があります。

最も人気のある機能は次の通りです：

・[LNURL-pay](https://github.com/lnurl/luds/blob/luds/06.md): ユーザーがLNURL-payのQRコードをウォレットでスキャンすると、支払者にLNインボイスが発行されます。このインボイスは金額を固定にするか範囲指定が可能で、支払い者はメッセージを残すこともできます。<br>
　・[LNURL-pay-to-Lightning-Address](https://github.com/lnurl/luds/blob/luds/16.md): ユーザーは、satoshi@your.domain のような電子メールアドレスのように見える、静的で人間が読めるインターネット識別子に対して支払いを行うことができます。この識別子は[ライトニング・アドレス](https://lightningaddress.com/)と呼ばれます。この機能を提供したいサービスは、pay-to-lightning-address、receive-to-lightning-address、またはその両方をサポートすることができることを覚えておいてください。<br>
・[LNURL-withdraw](https://github.com/lnurl/luds/blob/luds/03.md): LNサービスは、LNURLの「エンドポイント」（あるいは送金先）をQRコードで生成します。ユーザーはこのQRコードをスキャンし、引き出し可能な資金の最小額と最大額などの情報を受け取ります。金額が指定されると、ウォレットはLNインボイスをサービスに返し、支払いを待ちます。<br>
・[LNURL-auth](https://github.com/lnurl/luds/blob/luds/04.md): この機能により、ユーザーはLNウォレットの公開鍵で「ログイン」メッセージ（QRコードまたはテキスト文字列の請求書として提示）に署名することで、LNURLをサポートするサービスにログインできます。

![](/_images/glossary-number_1.png)

例：[stacker.news](https://stacker.news/) はログインプロセスでLNURL-authを有効にしています。

LNURLについてもっと知るためのリソース:

・[bolt.fun LNURL Guide](https://bolt.fun/guide/web-services/lnurl)<br>
・[bitcoin.design Payment Request Formats Guide](https://bitcoin.design/guide/how-it-works/payment-request-formats/#lnurl)<br>
・[BOLT 12 AND LNURL: WHAT IS THE FUTURE FOR BITCOIN’S LIGHTNING NETWORK?](https://bitcoinmagazine.com/technical/bolt12-lnurl-and-bitcoin-lightning)<br>
・[Awesome LNURL](https://github.com/lnurl/awesome-lnurl)


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
