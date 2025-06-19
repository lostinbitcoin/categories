---
title: イニシャル・ブロック・ダウンロード (IBD)
taxonomy:
    category:
        - glossary
---

## Initial Block Download (IBD)
2,100 sats

<div><button class="zap-button" data-npub="npub1x3x7spzvt6yflg4l825agplakkyv8h62h5jsl9qq7ghxlcr490wqz4qfw6" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/sishamo_moyashi">@sishamo_moyashi</a></div>

イニシャル・ブロック・ダウンロード（IBD）は、完全な[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)ブロックチェーンをゼロから構築するプロセスです。新しい[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node/)をセットアップしてビットコインネットワークに参加すると、他のノードに接続して[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)をリクエストします。新しいノードは過去に生成された全てのブロックをダウンロードおよび検証して[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)を構築し、ネットワークと同期します。

ブロックは個別ノードから得ますが、異なるノードからのデータとクロスチェックできること、さらには[プルーフオブワーク](https://lostinbitcoin.sakuraweb.com/glossary/pow/)・ブロックチェーンの性質から、IBDはトラストレスなプロセスです。IBDの速さはインターネットの帯域幅とコンピューターの仕様で異なり、場合によっては数日、数週間かかります。

IBDを開始すると、ノードはまず他のノードからすべての[ブロックヘッダー](https://lostinbitcoin.sakuraweb.com/glossary/block_header/)を収集し、次に各フルブロックをリクエストします。これはIBDの効率を高め、ユーザーがより早くノードを使用できるようにするためです。ビットコインノードはブロックを1個1個ダウンロードおよび検証することでブロックチェーンを構築すると同時に、[UTXO](https://lostinbitcoin.sakuraweb.com/glossary/utxo/)セット（すべての有効なビットコインの包括的なリスト）も構築します。UTXOセットはブロック内の[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)がUTXOを破棄および作成するたびに更新されます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
