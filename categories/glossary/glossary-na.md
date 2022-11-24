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

### <a id="na"></a>な

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="difficulty"></a>難易度| Difficulty|The difficulty is a measure of how hard it is to mine a block. In order to mine a block, miners must provide Proof-of-Work in the form of a valid hash of the block they intend to publish. A hash is essentially a large number, and for a hash to be valid, it must be smaller than a defined target number. This target number determines the difficulty of mining and is set by Bitcoin’s ruleset. This difficulty is dynamic: it updates every 2016 blocks—roughly 2 weeks—to ensure Bitcoin blocks come in roughly every 10 minutes. If more miners join the network and mine blocks at a faster rate, difficulty will rise. If miners stop mining, and blocks arrive slower than every 10 minutes, difficulty will fall. The difficulty therefore directly follows the trend in hash rate of the network. In a technical sense, the Bitcoin network sets the target rather than the difficulty. All valid Proofs-of-Work must be below this target. The difficulty then, is simply the inverse of the target. If the target is raised, this makes it easier for miners to find a hash below the target, so the difficulty has been lowered. Likewise, if the target is lowered, the difficulty has been raised. The target is encoded as a part of each block header and is called the ‘bits’ of a block. This allows nodes to directly verify whether the Proof-of-Work provided for a block is lower than the target.| 2,100 sats  |
|<a id="double_spend"></a>二重支払い| Double Spend |A double spend occurs when someone is able to spend the same money twice, fooling one or more parties into believing they have been paid. Digital objects like files and text are easy to duplicate. However, duplication is not a desirable trait in money. This is the double spend problem: how can a receiver of digital money be sure that the money they were sent was not simultaneously sent to someone else? How can all members of a monetary network be sure others are not duplicating their money at will? Bitcoin solves the double spend problem by using a decentralized ledger which all users can access. When one user sends bitcoin to another, they destroy the coin they own and create a new coin owned by the receiver. The destruction of the sender’s coin is recorded for all to see, so that they can never send it to someone else.| 2,100 sats  |
|<a id="mnemonic"></a>ニモニック| Mnemonic| A mnemonic phrase is a list of 12-24 words used to back up a wallet. This phrase is a representation of a seed, which is the data that generates all of the keys in an HD wallet. A mnemonic phrase is also sometimes referred to as a seed phrase or recovery phrase. Mnemonic phrases are a Bitcoin standard introduced by BIP 39 which most wallets implement. Most wallets will also allow users to add their own unique passphrase onto the end of the list of words to further increase security. Mnemonic words are chosen from a defined list of 2048 words, and any combination of words is a valid mnemonic phrase which will generate a valid set of keys. Thus, the probability of correctly guessing someone’s mnemonic phrase is 1 in 2048^24 or 2.96 x 10^79 guesses.| 2,100 sats  |
|<a id="node"></a>ノード|  Node |  A node is a discrete member of a network which interacts with other nodes to form the network. A Bitcoin node is any computer that runs a Bitcoin implementation and stores the entire blockchain. Nodes validate, broadcast, and request new blocks and the mempool to and from peers in the network. If nodes run compatible software, consensus is achieved.Node count is vital to protecting the network from malicious or haphazard source code changes, reorganizations, and other protocol changes. | 2,100 sats  |
|<a id="non_custodial"></a>ノンカストディアル| Non-Custodial | ノンカストディアルソリューション（セルフカストディアルソリューションとも言います）は、秘密鍵を第三者に預けるのではなく、ビットコイン所有者自らが管理する保管方法です。<br>ビットコイン（の所有権証明である秘密鍵）を自己管理すれば、第三者にトランザクションを検閲されることはありません。そのため、取引所などのカストディサービス提供者や政府にビットコインを没収されるリスクとプライバシーを侵害されるリスクを回避できます。<br>ただし、秘密鍵の管理には責任が伴います。ビットコインを自己管理する場合、万が一秘密鍵にアクセスできなくなっても、誰もあなたを助けることはできません。秘密鍵のコピーを複数作成して別の場所に分散保管、複数のウォレットで分散管理、マルチシグの使用などの対策を講じることで、セルフカストディソリューションのセキュリティを強化できます。 | 2,100 sats  |

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
