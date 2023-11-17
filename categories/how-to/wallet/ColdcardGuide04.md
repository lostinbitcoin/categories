---
title: ハードウェアウォレットCOLDCARDで大事なビットコインを守ろう④～バックアップ＆リカバリ編～
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - beginner
---

## COLDCARDをセットアップして基本的な使い方を覚えよう！

<button class="zap-button" data-npub="npub1uyf6ghmjy8p8mnt8jhutgh4jtjvzn7euwjf4yvpwuzwan5jl8xysnvsmuw" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button>

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインを安全に管理するには |  ![Tag](/_images/tag.png)  |  初級  | ![Time](/_images/timer.png)  |  25分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は[@katakoto](https://twitter.com/katakoto) が制作、2023年2月に公開したものです。*

### ハードウェアウォレットCOLDCARDで大事なビットコインを守ろう④～バックアップ＆リカバリ編～

[前回の記事](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcardguide03/)で、COLDCARDの開封からセットアップ、Sparrow Walletを利用したBitcoinの受け取り・送金の方法を一通り解説しました。

皆さんの大事なBitcoinも、ビットコイナーいち押しの[ハードウェア・ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#hardware_wallet)COLDCARDに保管され、まずは一安心といった所でしょうか。

だが、この世界にはそんなビットコイナーの心の平穏をかき乱すひとりのもじゃもじゃアフロがいた…

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">This is going to be the greatest finance movie ever made <a href="https://t.co/ltVnQSPq0p">pic.twitter.com/ltVnQSPq0p</a></p>&mdash; LilMoonLambo (@LilMoonLambo) <a href="https://twitter.com/LilMoonLambo/status/1595279597238734848?ref_src=twsrc%5Etfw">November 23, 2022</a></blockquote>

すでにAmazonでの映像化が決定している業界騒然のFTX崩壊事件を経て、**”Not your keys, Not your Bitcoin.”（自分の[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#private_key)でないなら、それは自分のBitcoinではない）**の機運が、これまでで一番の盛り上がりを見せています。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">1月3日は <a href="https://twitter.com/hashtag/%E3%83%93%E3%83%83%E3%83%88%E3%82%B3%E3%82%A4%E3%83%B3?src=hash&amp;ref_src=twsrc%5Etfw">#ビットコイン</a> の最初の[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#block)が生成された記念日。アンドレアスさんの有名なこの台詞に字幕を付けましたので、この大事なルールを今一度、皆で思い出しましょう！<a href="https://twitter.com/hashtag/NotYourKey?src=hash&amp;ref_src=twsrc%5Etfw">#NotYourKey</a> <a href="https://twitter.com/hashtag/NotYourBitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#NotYourBitcoin</a>　<a href="https://twitter.com/hashtag/HappyGenesisDay?src=hash&amp;ref_src=twsrc%5Etfw">#HappyGenesisDay</a> <a href="https://t.co/1C1rLrZRmh">pic.twitter.com/1C1rLrZRmh</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1212918529587961856?ref_src=twsrc%5Etfw">January 3, 2020</a></blockquote>

ですが、この連載においてBitcoinの**セルフ・カストディ（自己管理）**において最も重要なポイントが、いまだカバーされておりませんでした。そうそれは

### シードフレーズ（12もしくは24英単語）って結局何なのさ？

![ColdCardGuide04_1.jpg](/_images/ColdCardGuide04_1.jpg)

今回はCOLDCARDのセットアップ時に、言われるがままに書き留めたこの24単語(もしくは12単語)、[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#seed)フレーズの扱い方、正しい保管方法とそのリカバリについてのお話です。

Bitcoinの世界では、今まで聞いたことのないような新しい用語の数々であふれています。

シードフレーズ、ニーモニック・フレーズ、リカバリー・フレーズ、バックアップ・フレーズ・・・

そしてこれら全てが同一のものを指すなどと聞かされた日には、日々の暮らしに忙しい我々の頭は少なからず混乱し、そこから先への学習意欲をそがれてしまっても、それは無理もないことです。

![ColdCardGuide04_2.jpg](/_images/ColdCardGuide04_2.jpg)

ここはシンプルに、もっと端的に言い切ってしまいましょう。

**シードフレーズ、この大元は単なるバカでかい数字**です。もっと具体的に言うなら・・・　

115,792,089,237,316,195,423,570,985,008,687,907,853,269,984,665,640,564,039,457,584,007,913,129,639,936

この数字からどうぞご自由に好きなのを一個選んできてください。それが、あなたのシードフレーズになります。数字の大きさがイメージしにくければ、こんな想像をしてみましょう。

> あなたはこの宇宙を創造した神です。人智を超えたその能力により考えうるあらゆる場所に移動することができます。几帳面なあなたは、観測可能なこの宇宙に存在する原子の一個一個に通し番号を振りました。では、神よ。くじ引きの要領で一個、どれでも好きな原子を選んできてください。その原子にふってある番号、それがあなたのシードフレーズになります。
>

神はサイコロを振らないし、全知全能の神にBitcoinは必要ないかもしれませんが、我々人類には必要です。

どうして、この適当に選んできただけのただの数字でBitcoinのセキュリティが安全と言えるのか、たまたま他の人の選んだ数字とかぶることはないのか、そのあたりのお話はまた別の機会に。ここはひとまず「十分なランダムさを持って選ばれたこの大きな数字は、絶対に他の人が選んだ数字とかぶらない」と”トラスト”しておいてください。

これがどんなに"ぶつかりにくい数字"なのかを、皮膚感覚で体験したい方には、[こんな面白い読み物](https://alis.to/penyoo/articles/3k94QA4991lR)もあります。



そしてバカでかい数字のままでは人間には扱いにくいという理由で、少し細工をして我々が認識しやすい[英単語](https://github.com/bitcoin/bips/blob/master/bip-0039/english.txt)（もしくは[日本語](https://github.com/bitcoin/bips/blob/master/bip-0039/japanese.txt)）に変換したものが、このシードフレーズと呼ばれるものの正体です。

これまでシードフレーズを24個の英単語と言ってみたり、12個と言ってみたりどっちつかずの言い方をしてきましたが、これもどれぐらいの大きさの数字の中から、一つ選んでくるかというお話であり、別のたとえで言うなら、コインを256回投げて乱数を作るか、それとも半分の128回投げるかの違いになります。

そして現代の暗号化技術・情報セキュリティの考え方では、たとえ[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#wallet)作成時に12英単語のシードフレーズ(128bit エントロピー)を選んでも、その安全性には何ら問題ないとされています。

この円安の最中、けして安くはないハードウェア・ウォレットをわざわざ海外から輸入して、我々がやっている事は、言ってしまえばこのバカでかい数字を誰にも知られないように一生懸命守っているのに過ぎないのです。

ではこのシードフレーズを

- **絶対に他人に知られてはいけない**
- **極力デジタルデータ（Cloudに保存、デジカメ撮影 etc.）にしてはいけない**
- **WEBサイトに軽々しく入力してはいけない**

とよく言われるのはなぜでしょうか。それは、**シード（種）**フレーズの名前が表しているように、このフレーズを手にした人は誰でも、本来あなたに属するBitcoin[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#address)を全て復元できてしまうからです。それはすなわち、他人にあなたのBitcoinを自由にコントロールされてしまうことを意味します。

このあたりを優しく説明したくて、著者は以前、次のようなポエムを詠んだことがあります。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">１２の言葉を正しく唱えると<br>不思議な種が現れる<br>この種はあっという間に巨木に成長し<br>無数に枝分かれしたその先々で、橙色した葉を宿す。<br><br>この葉っぱが、あなたの <a href="https://twitter.com/hashtag/Bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#Bitcoin</a><br><br>～ <a href="https://twitter.com/hashtag/Bitcoin?src=hash&amp;ref_src=twsrc%5Etfw">#Bitcoin</a> “ウォレット”を優しく説明する試み ～ <a href="https://t.co/I4ZmhYuCqR">pic.twitter.com/I4ZmhYuCqR</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1547026262488596481?ref_src=twsrc%5Etfw">July 13, 2022</a></blockquote>

Bitcoinには、我々になじみが深い銀行口座番号のような、生涯一貫して番号が変わらない”アカウント”は存在していません。もちろん同じアドレスを繰り返し使い続けることも可能ですが、これはプライバシーの観点から推奨されていません。Bitcoinを受け取る際には、むしろどんどん新しいアドレスを生成して、毎回違うアドレス宛に送ってもらえばよいのです。

その無数の受け取りアドレスを生み出す種となるのがシードフレーズ。

一見何の関連もないバラバラのアドレス上にあるBitcoinのかけら達も、元をたどれば必ず一つの種、シードフレーズにたどり着きます。Bitcoinウォレットは、この[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#blockchain)上に無数に散らばったBitcoinが、すべてあなたに紐づく資産であることを一括表示する役割と、各アドレス上のBitcoinの利用を許可する署名を行う機能を持つものです。

**一個の種から、一本の大きな木。その全部があなたのBitcoin。**

![ColdcardGuide04_3](/_images/ColdCardGuide04_3.jpg)

Source: [https://twitter.com/MemeingBitcoin/status/1599429042083876865](https://twitter.com/MemeingBitcoin/status/1599429042083876865?s=20&t=iPosWjCO87RNsh8jZQMr1A)

より技術的な図解で理解したい方はTrezorのブログなどを参照してください。

![ColdcardGuide04_4](/_images/ColdcardGuide04_4.png)

Source: [https://trezor.io/learn/a/what-are-bips-slips](https://trezor.io/learn/a/what-are-bips-slips)

ここでは、シードフレーズのイメージとその重要性が以前より少しでもクリアに伝わったなら幸いです。

最近のメジャーなBitcoinウォレットは、ほとんどが**[BIP39](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-number/#bip39)**および**[BIP32](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-number/#bip32)**と呼ばれる業界標準に則って作成されているので、理論的に言えばBIP39&BIP32対応のハードウェア・ウォレットで作ったシードフレーズなら、復元時にはどのメーカーのものを使おうとも復元は可能です。（メーカー毎の復元時の差異に注意。巻末に復旧時に役立つサイトへのリンク集を用意しました。）

復元はハードウェア・ウォレットである必要もありません。BIP39&BIP32対応ソフトウェア上からの復元も可能です。（前回の記事でインストールした[Sparrow Wallet](https://sparrowwallet.com/)を使って復元することもできます。）

同じ環境で行えば、一つの種から毎回必ず同じ巨木が生えてくるイメージです。

COLDCARDも当然これらの業界スタンダードに準拠しているウォレットですので、シードフレーズの管理さえしっかりしていれば、いつでも必ず復元することができます。

となると、いかにしてオフライン環境でこのシードフレーズを死守するかが問題になってきます。盗難・紛失・火災・水没・破損 etc…神が人類に与えしあらゆる試練から守るには、付属のバックアップカードだけでは、少し心もとない気がしてきますよね。

そんな時、多くのビットコイナーが選んでいる方法はシンプルにズバリ

### **シードフレーズを鋼に刻む**

です。この方法はメタル・ウォレットと呼ばれ、すでにいくつかのプロダクトが販売され人気を博しています。

![ColdcardGuide04_5.png](/_images/ColdcardGuide04_5.png)

Source: [SeedPlate by Coinkite](https://bitcoinseedbackup.com/)

![ColdcardGuide04_6.png](/_images/ColdcardGuide04_6.png)

Source: [Hodlr Disks Bitcoin by hodlr.swiss](https://hodlr.swiss/products/seed-metal-backup-hodlr-disks-bitcoin)

どの製品を選んでも、ただの紙で保存するよりは格段に[耐久性](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#durability)があがります。とことんまで耐久性を見極めたい方は、Bitcoin Maxiとして有名な[サイファーパンク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#cypherpunk)Jameson Lopp師匠がとことんまでメタルウォレットを苛め抜く[「メタル・’ビットコインシードストレージ・ストレステスト」](https://blog.lopp.net/metal-bitcoin-seed-storage-stress-tests-round-v/)シリーズをご確認ください。

![ColdcardGuide04_7.jpg](/_images/ColdcardGuide04_7.jpg)

1090℃の熱で10分焼かれたかわいそうなHodl.Swissさん
Source：[https://blog.lopp.net/metal-bitcoin-seed-storage-stress-tests-round-v/](https://blog.lopp.net/metal-bitcoin-seed-storage-stress-tests-round-v/)

またどこまでも自律DIY精神あふるる日本のビットコイナーの中には、メタルウォレットを自作してしまう人たちまでいます。なんて稀有で気高い試み。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">頑丈！DIYメタルウォレット【電解エッチング】 by ロクヨウ <a href="https://t.co/npjOua0nTL">https://t.co/npjOua0nTL</a></p>&mdash; ロクヨウ (@Lokuyow) <a href="https://twitter.com/Lokuyow/status/1596734195136876544?ref_src=twsrc%5Etfw">November 27, 2022</a></blockquote>

デジタル空間にしか存在しないBitcoinを、我々人類は結局、金属板に刻んで保管するのかという、進化を逆戻りしているようなトホホな気分にもなりますが、今の所、物理空間でのこの安心感に勝るソリューションはまだないのです。

- **シードフレーズをオフラインで耐久性のある形で厳重に保管する**

これが、Bitcoinをセルフカストディする際の最も基本となる考え方となります。そして、この重要なシードフレーズを、一切のネット環境に触れることなく作成、保管まで行えるのがCOLDCARDを使う最大の利点とも言えます。

### シードフレーズからのリカバリ

では、さっそくあなたの魂に刻んだシードフレーズをCOLDCARDで復元してみましょう。

※ここでは新品のCOLDCARDへ新しいPINコードのセットアップが終わった状態からの復元を想定しています。手持ちのCOLDCARDでもこの工程を試すことは可能ですが、生成したシードフレーズを一旦破壊する必要があり、不十分な理解のまま進めると、最悪な場合、資金を失いかねないため、ここでは割愛します。

![ColdcardGuide04_8.jpg](/_images/ColdcardGuide04_8.jpg)

- **“Import Existing”**（既存のシードを読み込む）を選択します

![ColdcardGuide04_9.jpg](/_images/ColdcardGuide04_9.jpg)

- **“24 Words”**を選択します

![ColdcardGuide04_10](/_images/ColdcardGuide04_10.png)

- 1番目の単語の頭文字を選択、目的の単語になるまで選択を進めます
- 24番目まで同じ手順を繰り返します

![ColdcardGuide04_11](/_images/ColdcardGuide04_11.jpg)

- 全てのシードフレーズが正しく入力されると**“Applying…”**（適用中）の表示になります
- 初回設定時に行ったNFC/TAP機能とUSBポートの設定を再度行えば、復元完了

割愛したシードを破壊する工程を含む、リカバリー作業の流れを動画にまとめました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">COLDCARD シードフレーズ・リカバリー<br><br>🚨 復元環境を再現するために、動画内で&quot;Destroy Seed&quot;を行っていますが、新品のCOLDCARDで復元する際には不要です。シードフレーズを消去してしまう危険な行為ですので、資産の入っているウォレットなどでは安易に行わないようにしてください<br><br>TLDRポチポチ辛い <a href="https://t.co/NM11BUrcKB">pic.twitter.com/NM11BUrcKB</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1599546774456500224?ref_src=twsrc%5Etfw">December 4, 2022</a></blockquote>

簡単ですね！けれど、ここまで読み進められた方の中には、まだ何かが心にひっかかっているかもしれません。

> 「シードフレーズが大事なのはわかった。COLDCARDが壊れても、盗まれても、失くしてしまっても、シードフレーズさえあれば、色々なハードウェア・ウォレットやパソコン上に簡単に復元できるのもわかった。でもそれって、そもそもシードフレーズが盗まれたら、何もかもが終わりって事じゃ？」
>

まさしくその通り。シードフレーズをいくら金属板に刻んで大事にしまっていようが、それが誰かの手に渡ったり、読み取られてしまった時点で、あなたのBitcoinはその人のものになります。

では、そうした事態に何か対抗できる手段はないものでしょうか？

それがあるんです。その対策の名は

### パスフレーズ

また新たな用語の登場にうんざりしているかもしれませんが、頑張ってついてきてください。

**シードフレーズ＋パスフレーズ**を自在に使いこなせれば、Bitcoinの自己管理時のセキュリティを格段にアップさせることができるようになります。

### Bitcoin管理のセキュリティを強化するパスフレーズとは？

COLDCARDにパスフレーズを設定すると、既存のシードフレーズと組み合わせて、まったく新しいウォレットを生成することができます。COLDCARDのパスフレーズは、アルファベットの大文字、小文字 - 数字 - 記号を自由に組み合わせて使うことができ、最長100文字まで設定可能です。

![ColdcardGuide04_12](/_images/ColdcardGuide04_12.jpg)

図のように、パスフレーズはCOLDCARDの本体のどこにも保存されないため、シードフレーズが漏洩したり、COLDCARDが盗難されハックされたような場合でも、安全に資産を守ることが可能になります。（その分、パスフレーズ自体の記録や保管方法もまた重要なポイントになります。）

またパスフレーズには「入力したパスフレーズが違います！」といった警告は存在しません。上記のルールに則ったパスフレーズなら、どんな値を入力しても必ず新たなウォレットが開きます。

例えば僕が「katakoto」というパスフレーズを設定し、作成されたウォレットにBitcoinを送金。次回、間違って「Katakoto」（頭文字が大文字）をパスフレーズとして入力すると、まったく違う空っぽのウォレットが開いてしまいます。そして僕の頭は大パニック。

![ColdcardGuide04_13.jpg](/_images/ColdcardGuide04_13.jpg)

「僕のマネーはどこに消えた！？」

でも、うろたえなくて大丈夫。いつでもパスフレーズを含まない元のウォレットに戻ることができますし、あなたの資産は変わらずビットコインブロックチェーン上にしっかり記録されています。

これまでのシード（種）フレーズのイメージで言うと、種のDNAをパスフレーズでいじることによって、全く別の巨木が生えてくるイメージです。

パスフレーズ適用後、どのウォレットが開いたかの簡単な確認方法も存在しますので後述します。

では早速、COLDCARDにパスフレーズを設定してみましょう。

#### パスフレーズの作成

![ColdcardGuide04_14.jpg](/_images/ColdcardGuide04_14.jpg)

- **“Passphrase”**(パスフレーズ)を選択します

![ColdcardGuide04_15.jpg](/_images/ColdcardGuide04_15.jpg)

```
BIP-39のシードワードにパスフレーズを追加することができます。これにより、可能な限りのパスフレーズに対して、全く新しいウォレットが作成されます。
```

- **✓ボタン**で進む。ここで**２**を押すと、このメッセージは次回から表示されなくなります

![ColdcardGuide04_16.jpg](/_images/ColdcardGuide04_16.jpg)

- **“Edit Phrase”**(フレーズを編集)でパスフレーズを作成可能。

![ColdcardGuide04_17.jpg](/_images/ColdcardGuide04_17.jpg)

- **１ボタン**でアルファベット入力モード。**２ボタン**が数字入力モード。**３ボタン**が記号入力モード。**４ボタン**でアルファベットの大文字・小文字の切り替え。**上下ボタン**で入力値を選択し、**左右ボタン**でカーソルを移動。**☓ボタン**で一文字消去。

![ColdcardGuide04_18.jpg](/_images/ColdcardGuide04_18.jpg)

- **“Add Word”**(単語を追加)を選ぶと、シードフレーズでも使われる単語集の中から選んでパスフレーズにすることが可能。一文字ずつの入力が面倒な場合に便利です。

![ColdcardGuide04_19.jpg](/_images/ColdcardGuide04_19.jpg)

![ColdcardGuide04_20.jpg](/_images/ColdcardGuide04_20.jpg)

- 選んだ単語は常に、それまでの入力したフレーズの最後に追加されます。

![ColdcardGuide04_21.jpg](/_images/ColdcardGuide04_21.jpg)

- 同じように数字を追加したい場合は**”Add Numbers”**(数字を追加)を選択。

![ColdcardGuide04_22.jpg](/_images/ColdcardGuide04_22.jpg)

- それまでの入力内容を全部消したい場合は**”Clear ALL”**(全てを消去)

![ColdcardGuide04_23](/_images/ColdcardGuide04_23.png)

- 再度、**”Edit Phrase”**を押して自分の利用したいパスフレーズと相違ないかを確認しましょう。注意点としてはスペース（ディスプレイ内で**␣**で表示）も一文字として認識されるので、きちんと自分の意図したパスフレーズになっているかを確認が必要です。

#### パスフレーズの適用

では、作成したパスフレーズをウォレットに適用して、新たなウォレットを開いてみましょう。

![ColdcardGuide04_24.jpg](/_images/ColdcardGuide04_24.jpg)

- **“APPLY”**(適用)を選択します

![ColdcardGuide04_25.jpg](/_images/ColdcardGuide04_25.jpg)

- パスフレーズが適用され、新しいウォレットが開きます

![ColdcardGuide04_26.jpg](/_images/ColdcardGuide04_26.jpg)

- この画面で表示されている**”fingerprint”**（指紋）が、現在、自分がどのウォレットを開いているのかを確認する際に必要な情報です。巨木の例えで言うなら、木々を識別するための年輪のようなものになります。

#### ウォレットの確認

COLDCARDに電源を入れ、PINコードを入力した状態では常に

**シードフレーズ + 空のパスフレーズ**

を入力した状態のウォレットが開きます。つまり、電源を入れ直せばいつでもCOLDCARDは最初のウォレットを表示してくれます。

では、今現在、自分がどのウォレットを開いているのか確認するにはどうしたらよいでしょうか。

それには、先ほど登場した”**fingerprint”**(指紋)を使います。

![ColdcardGuide04_27.jpg](/_images/ColdcardGuide04_27.jpg)

![ColdcardGuide04_28.jpg](/_images/ColdcardGuide04_28.jpg)

- **“Advanced/Tools” → “View Identity”** (ID確認)を選択します。

![ColdcardGuide04_29.jpg](/_images/ColdcardGuide04_29.jpg)

- 一番上に表示されている**”Master Key Fingerprint”**が、このウォレット特有の値です。Fingerprintから元のシードフレーズにたどることは不可能ですので、気軽にメモして大丈夫です。

![ColdcardGuide04_30.jpg](/_images/ColdcardGuide04_30.jpg)

- パスフレーズ”KATAKOTObaby”を適用した後のFingerprintはこのように変わっています。

![ColdcardGuide04_31.jpg](/_images/ColdcardGuide04_31.jpg)

- **“Secure Logout”**(安全なログアウト)を選択後、電源を入れ直すと、ウォレットは元の状態に戻っていることが確認できます。

![ColdcardGuide04_29.jpg](/_images/ColdcardGuide04_29.jpg)

### Sparrow Walletでマルチウォレット管理

では、ベースになるシードフレーズにパスフレーズを適用して作られた新しいウォレットは、どのように管理したらよいでしょうか。この場合にも、前回の記事で利用した[Sparrow Wallet](https://sparrowwallet.com/)を利用すれば簡単です。

先ほどの例で、”KATAKOTObaby”というパスフレーズを適用したウォレットは、Fingerprintが下記のようになりました。

![ColdcardGuide04_26.jpg](/_images/ColdcardGuide04_26.jpg)

この状態で、Sparrow Walletを開きます。（COLDCARDとPCはUSB接続しているものとします。）

![ColdcardGuide04_32.png](/_images/ColdcardGuide04_32.png)

- **“File”→ “Import Wallet”** (ウォレットをインポート)を選択します。

![ColdcardGuide04_33.png](/_images/ColdcardGuide04_33.png)

- **“Scan for Connected Devices”**(接続されているデバイスをスキャン)を選択すると、COLDCARDが一番上に表示されます。

![ColdcardGuide04_34.png](/_images/ColdcardGuide04_34.png)

- **“Import Keystore”**(キーストアをインポート)を選択します。

![ColdcardGuide04_35.png](/_images/ColdcardGuide04_35.png)

- ウォレットの名前を付けて**”Create Wallet”**(ウォレットを作成)を選択し、パスワードを設定すれば、新たなウォレットがSparrow Walletで管理できるようになります。

![ColdcardGuide04_36.png](/_images/ColdcardGuide04_36.png)

- **“Settings”**(設定)から**”Master fingerprint”**を確認してみましょう。メモした先ほどの指紋と同じであることがわかると思います。

複数のウォレットで管理する際には、それぞれにわかりやすい名前を付けて、のちのち混乱を呼ばないようにしましょう。

元のウォレットのシードフレーズに、パスフレーズを組み合わせることで、それこそ無限とも言える自分だけのウォレットを即座に作り出すことができることが、おわかり頂けたでしょうか。

![ColdcardGuide04_38.jpg](/_images/ColdcardGuide04_38.jpg)
Source：[https://blog.coinkite.com/everything-you-need-to-know-about-passphrases/](https://blog.coinkite.com/everything-you-need-to-know-about-passphrases/)


繰り返しになりますが、パスフレーズの管理は、シードフレーズと同様に非常に大切です。その２つを同じ場所に保管していて盗まれたり見られたりした場合は、わざわざパスフレーズを設定した意味がなくなってしまいます。シードフレーズとは別の場所に保管するなどの工夫が必要です。

まずはシードフレーズから生成されたウォレットにしっかり慣れ親しみ、もうワンランク上のセキュリティが必要になった所で、パスフレーズ設定に挑戦してみてください。それら２つのウォレット間で少額のBitcoinをやり取りして練習すれば、もっと自信を持って使いこなせるようになるはずです。

パスフレーズを設定したウォレットは、金庫の中のさらなる隠し扉のような使い方ができます。おとりとして少額のBitcoinをシードフレーズのみによるウォレット側においておけば、そこから先へのクラッカーの侵入を防ぐ可能性もあるのです。　

![ColdcardGuide04_37.jpg](/_images/ColdcardGuide04_37.jpg)
Source：[https://www.sendaitansu.jp/SHOP/kc108.html](https://www.sendaitansu.jp/SHOP/kc108.html)

シードフレーズだのパスフレーズだの、この小さなデバイスでポチポチちまちま辛いですか？ならこれ買いましょう。Mk4の機能はそのままに、 QWERTYキーボード完備です。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Bitcoiners, please meet Q1 <a href="https://t.co/PVapuu9mbq">pic.twitter.com/PVapuu9mbq</a></p>&mdash; COLDCARD (@COLDCARDwallet) <a href="https://twitter.com/COLDCARDwallet/status/1623698350481760259?ref_src=twsrc%5Etfw">February 9, 2023</a></blockquote>

最終的にCOLDCARD新機種の宣伝になってしまいましたが、これまでの連載で一番伝えたかったのは

**"Bitcoinのセルフカストディ(自己保管)"は、けして難しくない。**

この一点です。現状のソリューションが最高とは、僕も思いません。これから自分たちの両親たちにも使えるようなより使いやすいこなれた製品、サービスなどが生まれてくるはずです。インターネットの進歩がまさにそうだったように。でも、せっかくこの初期段階にBitcoinに振れる機会があったのですから、この技術の真の意味での革命である **"Be your own Bank"(自分が自分の銀行になる)** 世界線にもぜひ足を踏み入れてみてください。

Bitcoinによる革新は、仲介者を排除し、人と人とを直接結び付けた価値交換を可能にした点にあります。その革新を巻き戻して再度、あなたと私の間に入り込もうとする人々・サービスを、それこそ容易にトラストしないようにしましょう。彼らは、そもそも、必要がない。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">「(クリプトの)自己保管を試みた人の99％が、資産を失うことになるという発言は、相対的リスクに対する重大で無責任な誤った決めつけである。<br><br>自分の富を知恵や専門知識と勘違いするのはやめて頂きたい。」<a href="https://twitter.com/hashtag/NotYourKeysNotYourCoins?src=hash&amp;ref_src=twsrc%5Etfw">#NotYourKeysNotYourCoins</a> <a href="https://t.co/W0d9lnCQAy">https://t.co/W0d9lnCQAy</a></p>&mdash; aantonop_quotes (@AantonopQuotes) <a href="https://twitter.com/AantonopQuotes/status/1603593132066902016?ref_src=twsrc%5Etfw">December 16, 2022</a></blockquote>

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">俺これ本人が「悪意ある切り取り。文脈を加味して」とか言ってるから、聞きたくもないのにAMA全部聞いたからな<br><br>ズレなく&quot;99%&quot;言ってるからな<br><br>もっと言うなら「NFTの将来性は？」に<br><br>「将来なんかもっとすごい事に使える。今はJPEGを売るだけだけど」<br><br>みたいな日本の情報商材屋と同じレベルだからな <a href="https://t.co/WESnbPISz4">https://t.co/WESnbPISz4</a></p>&mdash; katakoto (@katakoto) <a href="https://twitter.com/katakoto/status/1603979874414530560?ref_src=twsrc%5Etfw">December 17, 2022</a></blockquote>


通算4回に渡ってCOLDCARDの魅力をお伝えしてきたこの連載も、とりあえず今回でおしまいです。

この連載で説明できたのは、COLDCARDのごくごく基本的な機能に過ぎません。COLDCARDには、自身のセキュリティ管理レベルに応じて、さらに便利にさらにセキュアにBitcoinを管理するための機能がまだまだたくさんあります。

そうした機能もいつか「COLDCARD ～便利Tips編～」としてご紹介できれば嬉しいです。

それでは皆様、これからもBitcoin＋COLDCARDで安全安心なBitcoinライフをお送りください。

![ColdcardGuide04_39.jpg](/_images/ColdcardGuide04_39.jpg)
Source：[https://twitter.com/Annonymal_btc/status/1602279499701297152](https://twitter.com/Annonymal_btc/status/1602279499701297152)

> 「自分のマネーなのに個人情報が必要だとしたら、それはもはやマネーではない。社会信用度スコアシステムである。」  by Gigi
>



-------------------------------
参考サイト：
* [ビットコインアドレスを自分の手で作って理解する](https://nevertoolate.hatenablog.jp/entry/2020/04/02/060000)

* [Wallets Recovery(ウォレット互換性確認用)](https://walletsrecovery.org/)

* [Mnemonic Seed(シードフレーズ確認用)](https://learnmeabitcoin.com/technical/mnemonic)

* [COLDCARD 初心者向けガイド(公式)](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcard_beginner_guide/)

***
[利用規約 A](http://lostinbitcoin.jp.testrs.jp/staging/copyright/#uaa)
