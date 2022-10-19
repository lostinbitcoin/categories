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

### 索引 や

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="UTXO"></a>UTXO|  UTXO | An Unspent Transaction Output (UTXO) is a discrete piece of bitcoin. Bitcoin does not use accounts and balances. Instead, individual pieces of bitcoin are owned by individuals. Each UTXO has an amount associated with it. These are the discrete units of bitcoin which are spent and received in every transaction. When a UTXO is spent in a transaction it is destroyed, and one or more new UTXOs are created. All nodes maintain a set of existing UTXOs, called the UTXO set, which they update every time a block of transactions creates and destroys UTXOs. This allows nodes to independently verify whether a given transaction and the bitcoin it is attempting to spend are valid.　UTXOs are analogous to physical cash in that they usually require change when spent. If Alice owns a UTXO worth 1 BTC and wishes to pay Bob 0.4 BTC, she must spend the entire 1 BTC as an input. In order to send Bob exactly 0.4 BTC, Alice creates two outputs: the first to Bob, in the amount of 0.4 BTC, and the second back to herself, in the amount 0.59 BTC, assuming that she paid a 0.01 BTC transaction fee. This transaction will consume one UTXO and create 2 new ones. Note that the fee paid is not itself an output. It is implied by the sum of the inputs—1 BTC—minus the sum of the outputs—0.4 + 0.59 = 0.99 BTC. The miner of this transaction would calculate this fee and claim it for themself in the coinbase transaction.|  1,000 sats  |
| | |
| | |

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.