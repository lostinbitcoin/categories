---
title: コインセレクション
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Coin Selection
2,100 sats

コインセレクションとは、ウォレットが所有する[未使用トランザクションアウトプット（UTXO）](https://lostinbitcoin.jp/glossary/utxo/)の一部を選択して、取引を作成し資金を割り当てるプロセスのことを指します。ユーザーの代理で取引を作成する際には、ウォレットは特定のUTXOを選択して取引の資金源として使用する必要があります。

例えば、アリスがボブに1BTCを支払いたいとします。アリスがウォレットに様々な金額のUTXOを合計で5BTC保有している場合、ウォレットはどのUTXOを使用するかを決定しなければなりません。この決定は必ずしも単純ではなく、ユーザー（アリス）の優先事項によって異なります。コインセレクションの選択肢としては、[ダスト](https://lostinbitcoin.jp/glossary/dust/)（[送金手数料](https://lostinbitcoin.jp/glossary/transaction_fee/)に満たないくらい小さな額）の蓄積を避けるために、少額のUTXOを優先的に消費する方法や、大きなUTXOを使用して手数料を抑える方法があります。またプライバシーの強化や[チェンジ・アウトプット](https://lostinbitcoin.jp/glossary/change_output/)の発生を避けることを優先させる方法もあります。

コインセレクションは通常、[ウォレット](https://lostinbitcoin.jp/other/wallet/)に組み込まれたアルゴリズムによって制御されます。ただし、一部のウォレットではユーザー自身がコインセレクションの設定をカスタマイズして、自分のニーズに合った選択を行うことが可能です。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
