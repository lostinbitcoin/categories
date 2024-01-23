---
title: Jadeで完全エアギャップBitcoin送金
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - intermediate
---

## オフラインで生成した秘密鍵を一瞬たりともネットにさらさずBitcoinトランザクションに署名する方法

<div><button class="zap-button" data-npub="npub1uyf6ghmjy8p8mnt8jhutgh4jtjvzn7euwjf4yvpwuzwan5jl8xysnvsmuw" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/katakoto">@katakoto</a></div>

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインを安全に管理するには |  ![Tag](/_images/tag.png)  |  中級  | ![Time](/_images/timer.png)  |  30分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は[Ben Perrin](https://twitter.com/BTCsessions)氏の解説動画「[Unlocking ULTIMATE Security: Air-Gapped Bitcoin Transactions with Blockstream Jade!](https://youtu.be/XVKsaPCe260?si=4Zd0jl_HC-_iJr0H)」を参考に、[@katakoto](https://twitter.com/katakoto) が制作、2023年11月に公開したものです。*


![JadeAirgapGuide_000](/_images/JadeAirgapGuide_000.png)

### **「あなたの秘密鍵なら、あなたのビットコイン。あなたの秘密鍵でないなら、それはあなたのビットコインではない。」**

ビットコインの[セルフカストディ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-na/#non_custodial)(自己管理)に興味を持つ人なら、今では誰でも一度は聞いたことがあるこの有名なフレーズ。ビットコインの技術的側面に興味がある人の教科書とも言える「マスタリング・ビットコイン」の著者、アンドレアス・アントノプロス氏の言葉です。

それでも彼がこのフレーズを使い始めた当初は、その言葉の真意を知る人は今ほど多くはありませんでした。

「なんだかんだ言っても、取引所に預けておいた方が安心っしょ。」

多くのユーザーがそう思っていたし、今でもそうした考え方は多く残っています。がしかし

> Celsius Network: 暗号通貨融資プラットフォーム。2022年11月10日に米国で破産申請。
FTX:暗号通貨取引所大手。2022年11月11日に米国で破産申請。
Genesis: 暗号通貨ヘッジファンド。2022年11月15日に米国で破産申請。
BlockFi: 暗号通貨レンディング大手。2022年11月20日に米国で破産申請。
>

繰り返される数々の苦い実体験を経て、人は徐々に自分の財産を自分自身で管理することの意味とそのありがたみを理解していきます。

そして自然にたどり着く[ハードウェア・ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#hardware_wallet)という管理方法。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">What is the best hardware device? <a href="[https://twitter.com/hashtag/BTC?src=hash&amp;ref_src=twsrc^tfw](https://twitter.com/hashtag/BTC?src=hash&amp;ref_src=twsrc%5Etfw)">#BTC</a> <a href="[https://t.co/yrrHk64V0f](https://t.co/yrrHk64V0f)">[pic.twitter.com/yrrHk64V0f](http://pic.twitter.com/yrrHk64V0f)</a></p>— The ₿itcoin Therapist (@TheBTCTherapist) <a href="[https://twitter.com/TheBTCTherapist/status/1717701802835988482?ref_src=twsrc^tfw](https://twitter.com/TheBTCTherapist/status/1717701802835988482?ref_src=twsrc%5Etfw)">October 27, 2023</a></blockquote>

個人的には、このTweetに載っているどのデバイスを利用しても、自身で安全に資産を管理することができると思いますが、今回の記事ではさらにここから一歩踏み込んで **「エアギャップ」** という考え方に触れてみたいと思います。

## エアギャップとは

> **エアギャップ**[[1]](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%82%A2%E3%82%AE%E3%83%A3%E3%83%83%E3%83%97#cite_note-1)とは、コンピュータネットワークにおいて[セキュリティ](https://ja.wikipedia.org/wiki/%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF%E3%83%BB%E3%82%BB%E3%82%AD%E3%83%A5%E3%83%AA%E3%83%86%E3%82%A3)を高める方法の一つ。安全にしたいコンピュータやネットワークを、[インターネット](https://ja.wikipedia.org/wiki/%E3%82%A4%E3%83%B3%E3%82%BF%E3%83%BC%E3%83%8D%E3%83%83%E3%83%88)や安全でない[LAN](https://ja.wikipedia.org/wiki/Local_Area_Network)[[2]](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%82%A2%E3%82%AE%E3%83%A3%E3%83%83%E3%83%97#cite_note-2)といったネットワークから物理的に隔離することを指す。エアギャップという語は、コンピュータやネットワークが、他のネットワークから（概念上の「空隙」で）電気的に切断されていることを意味している。
>

[Wikipedia](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%82%A2%E3%82%AE%E3%83%A3%E3%83%83%E3%83%97)より引用

皆さんご存知のように私達が当たり前のように日々利用しているインターネットは、ひどく汚れた世界です。

人間の妬み、嫉み、僻み、あらゆる悪意渦巻くインターネットと精神衛生上、あなたも少し距離を置きたくなったことはありませんか？

ビットコインさんだって実はそうなのです。

隙あらばあなたの[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#private_key)や[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#seed)フレーズを奪おうとしてくるスキャマーがうごめき、マルウェア、フィッィング詐欺、キーロガーなどのあらゆる脅威と日々隣合わせのネットの世界と、その保管場所をバッサリと切り離しておくことは、もっとも有効な資産防衛法のひとつです。

極論、ビットコインを日々こつこつと積み立てていく用途であるならば、自分のビットコイン = 秘密鍵を徹頭徹尾、インターネットに触れさせることなく運用することが可能です。

その辺はこれまで自分の連載で紹介してきたCOLDCARDのお家芸ではあるのですが、今回はよりリーズナブルにこの「エアギャップ」運用が可能なBlockStream社のハードウェウォレット **「[Jade](https://blockstream.com/jade/)」** を使った方法を紹介してみたいと思います。

## BlockStream社製ハードウェウォレット「Jade」

BlockStream社の創業者アダム・バック博士は、サトシ・ナカモトによるBitcoinの[ホワイトペーパー](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#whitepaper)にも引用されているHashcashの発案者として有名な暗号学者であり、同社は[Bitcoin Core](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#bitcoin_core)への多大な貢献でも知られているBitcoin企業です。

そんな同社が開発したBitcoin用ハードウェウォレット「Jade」は、セキュリティと使いやすさにも定評がある上に、ソフトウェアは完全にオープンソース化されており、世界中のビットコイナーが常に **”Dont’ trust, verify.”**(信用するな、検証しろ)の目を光らせています。

デバイスは、小さいながらもカラー液晶ディスプレイとQRスキャン用カメラを備えているのが特徴で、今回の記事で紹介する **「Jade完全エアギャップBitcoin[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#transaction)」** も、この内蔵カメラをフル活用した方法となっています。

このガイドでは、海外のビットコインエデュケーターとして著名な[@BTC Sessions/Ben](https://twitter.com/BTCsessions)氏のご快諾の元、解説動画「[Unlocking ULTIMATE Security: Air-Gapped Bitcoin Transactions with Blockstream Jade!](https://youtu.be/XVKsaPCe260?si=4Zd0jl_HC-_iJr0H)」を参考に、サムネ画像入りで詳しく解説していきます。

![JadeAirgapGuide_001](/_images/JadeAirgapGuide_001.png)

## 今回の目的とポイント

- Jadeを利用し、一切インターネットに接続しない方法でウォレットを作成し、ビットコインを保管する。
- シードフレーズ(秘密鍵)も、Jade内には保存させない。
- ビットコイン送金時の署名は、毎回、携帯のモバイルウォレットとJade間でQRコードを経由して行う。これにより完全エアギャップ・トランザクションを実現する。

※この方法は、あくまで上級者を目的としたJadeの応用機能です。従来のハードウェウォレットのように、シンプルにシードフレーズをJade本体に保管しておく使い方も、もちろん可能です。

※またすでにJadeをお持ちで、従来の方法でウォレットをご使用中の場合は、デバイスを初期化する必要があります。この際、デバイス内の秘密鍵はすべて消去されてしまいます。この機能を試される方は、シードフレーズのバックアップを確実に行い、自己責任にてお願いいたします。

## 事前準備

まずはJade本体のファームウェアを最新版にアップデートします。”完全エアギャップ”を謳いながら最初からなんですが、今後PCの使用はこれのみです。

公式サイトから各自、自分のOS用「[Blockstream Green](https://blockstream.com/green/)」をダウンロード＆インストールしてください。

![JadeAirgapGuide_002](/_images/JadeAirgapGuide_002.png)

ソフトウェアを起動した状態で、JadeをUSB-Cケーブルにて接続すると、ファームウェア・アップデート用のウィザードがポップアップされるはずです。

![JadeAirgapGuide_003](/_images/JadeAirgapGuide_003.png)

Jade本体で承認（☑を選択）すると、本体は自動的にアップデートされます。

![JadeAirgapGuide_004](/_images/JadeAirgapGuide_004.jpg)

![JadeAirgapGuide_005](/_images/JadeAirgapGuide_005.jpg)

ここから先は、充電済のJadeであれば今後一切ケーブルを繋ぐ必要はありません。

では、Ben氏の解説の下、 **「Jade完全エアギャップBitcoinトランザクション」** 用セットアップを進めていきましょう。

## 必要なもの

- [Jade本体](https://store.blockstream.com/product/blockstream-jade-hardware-wallet/)
- [QRコードテンプレート](https://help.blockstream.com/hc/article_attachments/20515645709593)（公式サイトから印刷可）
- マジックペン
- iPhone or Android携帯
- [Nunchukモバイルウォレット](https://nunchuk.io/) (各自インストールしておいてください)

## QRシードコードの作成

![JadeAirgapGuide_006](/_images/JadeAirgapGuide_006.png)

- Jade右下の電源ボタンを数秒押して、電源を入れます。
- 「Setup Jade」→ 「Continue」→ 「Advanced Setup」を選択します。

![JadeAirgapGuide_007](/_images/JadeAirgapGuide_007.png)

- 「Continue」→ 「Create New Wallet」（新しいウォレットの作成）を選択します。
- 「12 Words」を選択し、下記の注意書きを確認して「Continue」を選択します。

> These words are your wallet. Keep them protected and offline.
この単語があなたのウォレットです。オフラインで大切に保管してください。
>

![JadeAirgapGuide_008](/_images/JadeAirgapGuide_008.png)

- 12単語が4単語ずつ表示されます。順番に書き留めていきましょう。
- 上部のホイールで次へ進んだり、前に戻ったりできます。
- 12単語をすべて書き留めると確認画面になります。

![JadeAirgapGuide_009](/_images/JadeAirgapGuide_009.png)

- 確認画面では、２つの単語の間に入る正しい単語をホイールで選択して答えます。
- 写真の例では４と６の間の単語、つまり５番目の単語を選択しています。
- すべての確認作業に正解すると、設定画面は次に進みます。

![JadeAirgapGuide_010](/_images/JadeAirgapGuide_010.png)

> Export recovery phrase as a CompactSeedQR
リカバリーフレーズをコンパクトSeedQRとしてエクスポートしますか？
>

- 「Yes」を選択します。

![JadeAirgapGuide_011](/_images/JadeAirgapGuide_011.png)

> Draw the CompactSeedQR for use with QR Mode
コンパクトSeedQRをQRモードで使用するため書き出しますか？
>

- 「Yes」を選択します。

![JadeAirgapGuide_012](/_images/JadeAirgapGuide_012.png)

- SeedQRの全体図が表示されます。転写するために、ここから４分割していきます。
- 「Start」を選択して開始します。

![JadeAirgapGuide_013](/_images/JadeAirgapGuide_013.png)

![JadeAirgapGuide_014](/_images/JadeAirgapGuide_014.png)

- 最初の「A1グリッド」は、すでに塗りつぶされているはずなので、このまま進みます。

![JadeAirgapGuide_015](/_images/JadeAirgapGuide_015.png)

- ホイールを回して「A2グリッド」へと進みます。
- 黒いドットで表示されている箇所を、マジックペンで塗りつぶしていきます。
- この際、マス目のすべてを塗りつぶす必要はなく、点を打つ要領でOKです。

※後半での打ち間違いは結構悲しい気分になるので、鉛筆などでの下書きをおすすめします。

![JadeAirgapGuide_016](/_images/JadeAirgapGuide_016.png)

- 同じ要領で「A3グリッド」→「B1グリッド」→ … → 「C3グリッド」まで書き写します
- ホイールを右or左に回してOKボタンを押すと、いつでも別のグリッドに移動できます。

![JadeAirgapGuide_017](/_images/JadeAirgapGuide_017.png)

- SeedQRが完了したら「Done」を押して完了します。次はしっかりスキャンできるかの確認です。

![JadeAirgapGuide_018](/_images/JadeAirgapGuide_018.png)

- 作成したQRコードがきちんとスキャンできるかを確認します。
- カメラをQRコードに近づけすぎると読み取れないので、少し遠目からスキャンするのがコツです。

![JadeAirgapGuide_019](/_images/JadeAirgapGuide_019.png)

- スキャンが成功すると「QR Code Verified」(QRコードが確認されました)と表示されます。
- 「Continue」を押して進みます。

![JadeAirgapGuide_020](/_images/JadeAirgapGuide_020.png)

- パスフレーズを設定するかどうかの確認画面です。設定する場合は「Yes」を選択。

> Add BIP39 passphrase? You will need this to access your funds.
[BIP39](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-number/#bip39)パスフレーズを追加しますか？自身の資金にアクセスする際に必要になります。
>

現状では、QRコードを他の誰かにスキャンされてしまうとあなたの資金はすぐに盗まれてしまう状態にありますが、「パスフレーズ」を設定することでそうした事態を防ぐことができます。

パスフレーズに関する詳しい解説は、過去の[こちらの記事](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcardguide04/)をお読みください。

![JadeAirgapGuide_021](/_images/JadeAirgapGuide_021.png)

- 好きなパスフレーズを設定します。（この例では”abc”で設定しています。）
- ☑マークを押して決定します。

![JadeAirgapGuide_022](/_images/JadeAirgapGuide_022.png)

- 確認画面で、パスフレーズを確認します。問題なければ「Yes」を選択します。

![JadeAirgapGuide_023](/_images/JadeAirgapGuide_023.png)

- 他のデバイスとJadeの接続方法を選択します。今回は「完全エアギャップ」なので「QR」を選択です。

![JadeAirgapGuide_024](/_images/JadeAirgapGuide_024.png)

> Save and encrypt wallet with PIN or scan a SeedQR every session?
暗号化したウォレットを保存しPINで使用しますか？
それとも使用する度にSeedQRをスキャンしますか？
>

- 「SeedQR」を選択します。

![JadeAirgapGuide_025](/_images/JadeAirgapGuide_025.png)

> This wallet will be temporary and forgotten on reboot.
このウォレットは一時的なものとなり、再起動ごとに消去されます。
>

- つまり秘密鍵はJade本体には保存されないことを意味します。「Continue」で進みます。

![JadeAirgapGuide_026](/_images/JadeAirgapGuide_026.png)

- ひとまず、これでJade側の設定は完了です。この画面は「自身の秘密鍵」＋「パスフレーズ」を入力してログインしている状態です。

## Nunchukモバイルウォレットのセットアップ

![JadeAirgapGuide_027](/_images/JadeAirgapGuide_027.png)

- ウォレットにログインした状態のJadeで「Options」を選択します。

![JadeAirgapGuide_028](/_images/JadeAirgapGuide_028.png)

![JadeAirgapGuide_029](/_images/JadeAirgapGuide_029.png)

- 「Wallet」→ 「Export Xpub」を選択します。

![JadeAirgapGuide_030](/_images/JadeAirgapGuide_030.png)

- Nunchukモバイルウォレットで読み込むためのアニメーションQRコードが表示されます。

![JadeAirgapGuide_031](/_images/JadeAirgapGuide_031.png)

- 携帯にインストールしておいたNunchukウォレットを起動します。
- 「Keys」の「＋」マークをクリックします。

![JadeAirgapGuide_032](/_images/JadeAirgapGuide_032.png)

- 「Add air-gapped key」(エアギャップ・キーの追加)を選択します。

![JadeAirgapGuide_033](/_images/JadeAirgapGuide_033.png)

- 解説画面を「Continue」でスキップしたら、このキーに名前を付けましょう。
- 「Scan QR」をクリックすれば、JadeのQRコードのスキャニングが開始できます。

![JadeAirgapGuide_034](/_images/JadeAirgapGuide_034.png)

- 携帯のカメラへのアクセスに許可を与え、JadeからQRコードをスキャンしてください。

![JadeAirgapGuide_035](/_images/JadeAirgapGuide_035.png)

- 「Add Key」をクリックしてキーを追加します。

![JadeAirgapGuide_036](/_images/JadeAirgapGuide_036.png)

- 「Done」をクリックすれば、キー追加の設定が完了です。

![JadeAirgapGuide_037](/_images/JadeAirgapGuide_037.png)

- このキーをウォレットにリンクしましょう。「Wallet」欄の「＋」をクリックします。

![JadeAirgapGuide_038](/_images/JadeAirgapGuide_038.png)

- 「Create New Wallet」をクリックしてウォレットに名前を付けます。
- 名前を入力したら「Continue」をクリックして進みましょう。

![JadeAirgapGuide_039](/_images/JadeAirgapGuide_039.png)

- 先程追加したキーを選択して「Continue」をクリックすれば、このキーを利用したウォレットが作成されます。

![JadeAirgapGuide_040](/_images/JadeAirgapGuide_040.png)

- レビュー画面で、このウォレットがひとつのキーを利用した、一般的なウォレットであることが確認できます。「Continue」をクリックして進みます。

![JadeAirgapGuide_041](/_images/JadeAirgapGuide_041.png)

- この画面では、ウォレット設定のバックアップ画面ですが、今回のセットアップでは必要ありませんので「I'll do this later」(あとでやります）を選んでOKです。

※[マルチシグ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ma/#multisig)・ウォレットを作成するような場合は、このバックアップが後の復元時に非常に重要になります。

![JadeAirgapGuide_042](/_images/JadeAirgapGuide_042.png)

お疲れ様でした。これでJadeで生成した秘密鍵とリンクしたNunchukモバイルウォレットの設定が完了しました。

![JadeAirgapGuide_043](/_images/JadeAirgapGuide_043.png)

Bitcoinの受け取りはとても簡単です。

![JadeAirgapGuide_061](/_images/JadeAirgapGuide_061.png)

ウォレット名をクリックして「Recieve」(受け取り)をクリックすれば、いつでもウォレットに紐づく新たなアドレスが表示されます。

アドレスが本当にこのシードフレーズから生成されたものなのか心配で確認したい方はJadeを使ってVerify(検証)することもできます。

![JadeAirgapGuide_062](/_images/JadeAirgapGuide_062.png)

ウォレットにログインしている状態で「Scan QR」を選択して、確認したいアドレスのQRをスキャンしてください。

![JadeAirgapGuide_063](/_images/JadeAirgapGuide_063.png)

アドレスが表示されるので☑を選択すれば「Adress verified」(アドレス検証済)と表示され、自身のアドレスであることが確認できます。



## エアギャップ・トランザクションによるBitcoin送金

さあ、ここからがこのセットアップの真骨頂とも言えるエアギャップ・トランザクションによるBitcoinの送金の解説です。

ここで、今一度確認ですが、Jadeの電源を切った時点であなたの秘密鍵は、Jade本体から消去されます。

この世界の誰もあなたの秘密鍵は、設定時にメモしたQRコードとシードフレーズからしか知りようがありません。

そしてポイントは、あなたの秘密鍵は設定時から一度も、インターネットには触れていない点です。そして今や、Jade本体内にも保存されていません。かつBitcoinを受け取る際には、秘密鍵を出し入れする必要が一切ない。

それでは、再度、秘密鍵が必要になる場面は何でしょうか。

そう、それがBitcoinを送金する場面なのです。

では、参ります。

![JadeAirgapGuide_044](/_images/JadeAirgapGuide_044.png)

- Jadeの電源を入れ、「Scan SeedQR」を選択します。

※画面下部のUninitialized(未初期化）が、Jade本体に何も保存されていない状態を示しています。

![JadeAirgapGuide_045](/_images/JadeAirgapGuide_045.png)

- カメラでQRコードをスキャンします。

![JadeAirgapGuide_046](/_images/JadeAirgapGuide_046.png)

- 設定時にパスフレーズを設定した場合は、ここでパスフレーズを入力します。
- ☑を押して、完了です。（設定していない場合は、空欄のまま☑を押します。）
- パスフレーズの入力が正しいことを確認して「Yes」を選択します。

![JadeAirgapGuide_047](/_images/JadeAirgapGuide_047.png)

- これでウォレットにログインした状態になりました。この状態で、受金アドレスの確認や送金時の署名が可能になります。

※画面下部がActiveになっていて、右下にフィンガープリント(ウォレットの確認に使用)が表示されています。

では、モバイルウォレットに持ち替えて実際に送金トランザクションに署名してみます。

![https://kome.ai/kome-horizontal.svg](https://kome.ai/kome-horizontal.svg)

![JadeAirgapGuide_048](/_images/JadeAirgapGuide_048.png)

- Nunchukウォレットを開いて「Send」(送金)をクリックします。

![JadeAirgapGuide_049](/_images/JadeAirgapGuide_049.png)

- 画面右上のQRスキャンマークをクリックして、送金先アドレスをスキャンします。

![JadeAirgapGuide_050](/_images/JadeAirgapGuide_050.png)

- 送金金額を入力します。「Send all」をクリックすると全額送金になります。
- 送金金額を正しく入力したなら「Continue」をクリックして進みます。

![JadeAirgapGuide_051](/_images/JadeAirgapGuide_051.png)

- トランザクションの確認画面になります。宛先アドレスに間違いがなければ「Create transaction」(トランザクション作成)ボタンをクリックします。

![JadeAirgapGuide_052](/_images/JadeAirgapGuide_052.png)

- 「Sign」(署名)をクリックしましょう。

![JadeAirgapGuide_053](/_images/JadeAirgapGuide_053.png)

- 「Export transaction」(トランザクションのエクスポート)をクリックします。
- 「Export via QR」(QR経由でエクスポート)をクリックします。

![JadeAirgapGuide_054](/_images/JadeAirgapGuide_054.png)

- ウォレットにログインした状態のJadeで「Scan QR」を選択します。
- Nunchuk画面上に表示されるQRコードをスキャンしてください。
- 緑ゲージが100％になるとスキャンが完了します。

![JadeAirgapGuide_055](/_images/JadeAirgapGuide_055.png)

- 画面に送金アドレスと送金金額が正しく表示されているのを確認して「→」を選択します。

![JadeAirgapGuide_056](/_images/JadeAirgapGuide_056.png)

- Fee([送金手数料](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#transaction_fee))を確認し、問題なければ☑を選択します。
- QRコードが表示されているJade側の電源は切らずにそのままにしておきます。

※この時点でJadeによる署名は完了していますが、まだ送金手続きは完了していません。今度はNunchuk側で、この署名されたトランザクションを取り込む作業を行います。

![JadeAirgapGuide_057](/_images/JadeAirgapGuide_057.png)

- Nunchukウォレットに持ち替えて「Import signature」(署名のインポート)をクリックします。

![JadeAirgapGuide_058](/_images/JadeAirgapGuide_058.png)

![JadeAirgapGuide_059](/_images/JadeAirgapGuide_059.png)

- カメラに切り替わるので、携帯でJade画面上のQRコードをスキャンします。
- カメラはそれほど接近させる必要はありません。進捗状態が携帯上に1%～100%で表示されます。

![JadeAirgapGuide_060](/_images/JadeAirgapGuide_060.png)

- 100％スキャンが完了すると署名欄が「Signed」になり、送金の準備が完了です。
- 「Broadcast transaction」(トランザクションのブロードキャスト)をクリックすると、ビットコイン・ネットワークにトランザクションが送られ、実際のビットコインの送金が開始されます。

お疲れ様でした。これでJadeを利用した「完全エアギャップBitcoinトランザクション」の解説は終了です。

毎回、同じ結論になりますが、Jadeを利用したビットコイン保管においても、初期設定時にメモした12単語(シードフレーズ)の保管方法が、資産防衛のための最重要ポイントになります。

あわせて読みたい：[ハードウェアウォレットCOLDCARDで大事なビットコインを守ろう④～バックアップ＆リカバリ編～](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcardguide04/)

このセットアップでは、秘密鍵自体が一切デバイスに残らないため、このシードフレーズのオフライン管理は、なおのこと重要になります。

さらに今回は、手書きしたSeedQRコードの保管も加えて考える必要があるため、一般的なセルフカストディより注意する点が多くなりますし、このSeedQRコードも、スキャンされると一瞬で秘密鍵を盗まれてしまうのではないかと、不安要素のひとつに思うかもしれません。

しかし、実際はこのQRコード、一般的なQRコードの規格とは違い特殊なものなので、携帯カメラで読み取ろうとしても、そもそも反応しません。つまりSeedQRコードを、普通の携帯でスキャンしても、それですぐさまシードフレーズが読み取られるというわけではないのです。

また先述したパスフレーズの設定により、シードフレーズおよびSeedQRコードの流出時にも対策が可能です。

この点をうまく利用し、SeedQRコードをビットコインとの関連性を感じさせない形でうまく保管すれば、セキュリティと利便性をうまくバランスさせた形での運用が可能になると思います。

また送金時のやり取りを、少しまどろっこしく感じた方もいらっしゃると思いますが、この面倒臭さにこそ価値を見いだせる初中・上級者の方々には、ぜひおすすめしたい方法です。

しかし、もしもっと安価で簡単に「エアギャップBitcoinトランザクション」が実現できるプロダクトが他にもあったとしたら？


![JadeAirgapGuide_061](/_images/JadeAirgapGuide_061.jpg)

次回、「TAPSIGNER x Nunchukでもっと簡単エアギャップ！」乞うご期待。






***
[利用規約 A](http://lostinbitcoin.jp.testrs.jp/staging/copyright/#uaa)
