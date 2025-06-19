---
title: LNURL
taxonomy:
    category:
        - glossary
---

## LNURL
2,100 sats

<div><button class="zap-button" data-npub="npub1f3maxrcsh7ep5kcfjcvu7zl85far4qdjfgk7nz83gksr3k73r9hqaelayw" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/_LN_RN">@_LN_RN</a></div>

LNURLは、QRコードを活用してライトニングウォレット（以下、LNウォレット）と他のアプリケーションとの通信を簡素化します。通常、ビットコインを[ライトニング・ネットワーク](https://lostinbitcoin.sakuraweb.com/glossary/lightning_network/)上で送受金するには、[ライトニング・インボイス](https://lostinbitcoin.sakuraweb.com/glossary/lightning_invoice/)（以下、LNインボイス）と呼ばれる長い文字列を受金者が生成して送金者に提供することが求められます。LNURLは、こうした複雑なフローを抽象化することで、送受金時のユーザー体験を改善します。<br>
「LNURL」は技術的には、HTTPを活用してライトニング・ネットワーク上の送金を調整する複数のオープンソースの[プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)の一群を指します。

LNURLを導入すれば、対応サービスにLNウォレットでログインできるほか、一度しか使えないLNインボイスと異なり繰り返し使える固定の支払いコード、あるいはそのQRコードを送受金に活用できます。本稿執筆時点で、LNURLにはアプリケーションに実装可能な20の機能があります。

その中でも人気の機能は次の通りです：

・[LNURL-pay](https://github.com/lnurl/luds/blob/luds/06.md): LNURL-payのQRコードをLNウォレットでスキャンするとLNインボイスが発行されます。インボイスの金額は固定または範囲指定が可能で、送金者は受金者へのメッセージを含めることもできます。<br>
 ・[LNURL-pay-to-Lightning-Address](https://github.com/lnurl/luds/blob/luds/16.md): satoshi@your.domain のように一見するとeメールアドレスのような、覚えやすい固定のインターネット識別子を宛先とした送金を可能にします。この識別子は[ライトニング・アドレス](https://lightningaddress.com/)と呼ばれます。これを実装することで、pay-to-lightning-address、receive-to-lightning-address、またはその両方に対応できます。<br>
・[LNURL-withdraw](https://github.com/lnurl/luds/blob/luds/03.md): LNURLの「エンドポイント」（あるいは送金先）をQRコードで生成します。LNウォレットでQRコードをスキャンすると、受金可能な最小額と最大額などの情報を読み込みます。受金額を指定すると、LNインボイスが生成され、サービス提供者のサーバーに送信されます。しばらくすると指定した額のビットコインがLNウォレットに届きます。<br>
・[LNURL-auth](https://github.com/lnurl/luds/blob/luds/04.md): LNウォレットの公開鍵で「ログイン」メッセージ（QRコードまたは文字列のLNインボイス）に署名することで、LNURLをサポートするサービスにログインできます。

![](/_images/glossary-number_1.png)

例：[stacker.news](https://stacker.news/) はログインプロセスでLNURL-authを有効にしています。

LNURLについてもっと知るためのリソース:

・[bolt.fun LNURL Guide](https://bolt.fun/guide/web-services/lnurl)<br>
・[bitcoin.design Payment Request Formats Guide](https://bitcoin.design/guide/how-it-works/payment-request-formats/#lnurl)<br>
・[BOLT 12 AND LNURL: WHAT IS THE FUTURE FOR BITCOIN’S LIGHTNING NETWORK?](https://bitcoinmagazine.com/technical/bolt12-lnurl-and-bitcoin-lightning)<br>
・[Awesome LNURL](https://github.com/lnurl/awesome-lnurl)


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
