---
title: ライトニング・ネットワーク
taxonomy:
    category:
        - glossary
---

## Lightning Network
2,100 sats

ライトニング・ネットワーク（Lightning Network 略称LN）は[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)を即時かつ安価に送金できるように設計された[プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)です。ライトニング・ネットワークはまだ実験的な段階にありますが、ビットコインの[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)処理能力を増強することが期待できます。このプロトコルは双方向のペイメントチャネルを中心に構築されており、2者間の相互送金を可能にします。また、ペイメントチャネルで直接接続されていない2者間でも、複数チャネルを中継することで相互に送金できます。

双方向ペイメントチャネルの開設には、[オンチェーン](https://lostinbitcoin.sakuraweb.com/glossary/on_chain/)上で2者で作った[マルチシグ](https://lostinbitcoin.sakuraweb.com/glossary/multisig/)アドレスへビットコインを送ることが必要です。マルチシグアドレスのビットコインは、ライトニング・ネットワーク上で使う限り、オンチェーン上でのビットコインの移動を伴わず（[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)にトランザクションを記録せず）、2者間で瞬時かつ無料で送金できます。

例えば、アリスとボブがそれぞれ0.5BTCずつ合計1BTCをマルチシグアドレスへ拠出した場合、ライトニング・ネットワーク上の2人の残高はそれぞれ0.5BTCとなります。この際、インプットがマルチシグアドレスの1BTC、アウトプットがアリスに0.5BTC、ボブに0.5BTCというトランザクションが作成されます。アリスがボブに0.1BTCを送ると、トランザクションはインプットはそのままで、アウトプットがアリス0.4BTC、ボブ0.6BTCに更新されますが、まだビットコインネットワークに送信されません。アリスとボブは必要に応じて送金を続け、何度でもトランザクションを更新できます。2人がペイメントチャネルを閉じる時に初めて、最後に更新した最新トランザクションがビットコインネットワークに送信されます。このトランザクションによって、アリスとボブのライトニング・ネットワーク上での残高がそれぞれの[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet/)へ送金されます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
