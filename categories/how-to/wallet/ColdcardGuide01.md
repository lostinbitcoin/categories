---
title: ハードウェアウォレットCOLDCARDで大事なビットコインを守ろう⓵
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - beginner
---

## Ledger、Trezor ではなく、COLDCARD をおすすめする理由

<div><button class="zap-button" data-npub="npub1uyf6ghmjy8p8mnt8jhutgh4jtjvzn7euwjf4yvpwuzwan5jl8xysnvsmuw" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/katakoto">@katakoto</a></div>

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインを安全に管理するには |  ![Tag](/_images/tag.png)  |  初級  | ![Time](/_images/timer.png)  |  10分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は[@katakoto](https://twitter.com/katakoto) が制作、2022年7月に公開したものです。*

皆さんは大切な[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#bitcoin)を管理するのに、どんな[ハードウェアウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#hardware_wallet)を使っていますか？

SATOSHILABS社の[Trezor](https://trezor.io/)？それともフランスLedger社の[Ledger](https://www.ledger.com/)？

日頃からクリプトをまるでおはじきの如くあっちにつま弾き、こっちにつま弾いてらっしゃる多く皆様にとっては、初めてのハードウェアウォレット選びの際には、この２つからどちらを選ぶかで悩んだ方が多かったのではないでしょうか。しかし、コアなビットコイナーにとってのもう一つのデファクト・スタンダード、もといオンリーオプションと呼べるハードウェアウォレットがあるのをご存じでしょうか。

その名は **「COLDCARD」**

![](/_images/ColdcardGuide01_1.jpg)

製品に付属するこのステッカーがすべてを物語っているように、2011年から **”ビットコイン・オンリー”** の製品を開発・販売しているカナダの[Coinkite社](https://coinkite.com/)が提供するハードウェアウォレットです。

![](/_images/ColdcardGuide01_2.jpg)

同社が作る製品の中には、元Twitter社CEOのジャック・ドーシー氏の米SNS公聴会動画の背後に写り込んでいて有名になった[Blockclock](https://blockclockmini.com/)（リアルタイムにビットコイン価格や[ブロック高](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#block_height)などを表示するビットコイン時計）などもあります。

![](/_images/ColdcardGuide01_3.png)

ソース：[https://www.youtube.com/watch?v=UipFasl_nD0&t=2516s](https://www.youtube.com/watch?v=UipFasl_nD0&t=2516s)

このように世界中のビットコイン愛好家、とりわけビットコインガチ勢から絶大な支持を得ているCoiknkite社のフラッグシップ製品でありながら、そのとっつきにくさから日本での知名度があまりないCOLDCARD。

この連載では、そんなCOLDCARDの魅力を皆さんにもっと知ってもらうべく、購入方法から基本的なセットアップ、使い方までを徹底解説して行きます！

### Why COLDCARD(なぜ僕らはCOLDCARDを使うのか)

筆者自身は長年のTrezor愛用者ですし、Ledgerもクリプト初心者に大変人気の高いハードウェアウォレットです。特にLedgerはフランス発ということもあってか、製品のデザインセンスも高く、最近ではFendi社とのコラボ製品を発表するなど、クリプトのマスアダプションに向け高級ブランドまでをも巻き込んでの快進撃を続けています。このキラキラ度合がまぶしすぎるあまり、日陰に生きる僕の視界からはいつの間にか見えなくなってしまいましたが（こうした現象をクリプト陽キャによるハレーション効果と呼びます。）どちらも、普段使いには何ら問題のない素晴らしい製品です。使いやすさだけで言うなら、現状はColdcardよりもこれらの製品に圧倒的に分があると言ってしまってもよいと思います。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Powering the Web3 revolution with <a href="https://twitter.com/Ledger?ref_src=twsrc%5Etfw">@Ledger</a>. Discover the <a href="https://twitter.com/hashtag/FendiXLedger?src=hash&amp;ref_src=twsrc%5Etfw">#FendiXLedger</a> collection, unveiled on the <a href="https://twitter.com/hashtag/FendiFW22?src=hash&amp;ref_src=twsrc%5Etfw">#FendiFW22</a> men’s runway. <a href="https://t.co/BfvZGQvROs">pic.twitter.com/BfvZGQvROs</a></p>&mdash; Fendi (@Fendi) <a href="https://twitter.com/Fendi/status/1482426260676567041?ref_src=twsrc%5Etfw">January 15, 2022</a></blockquote>

しかしここに普段からセキュリティやプライバシーに並々ならぬ関心を寄せ、「トラストレス」を人生の至上命令として生きるビットコイナー的視点が加わると、それまでのわかりやすくてキラキラと輝いていた平和な世界は、瞬く間に別の様相を表し始めるのです。

突然ですが、ここでハードウェアウォレット業界を揺るがしたある2つの事件について振り返ってみましょう。

### Trezorに5分内にシードが抜かれるパッチ不可能な脆弱性（2019年7月）

ライバル社Ledgerのセキュリティ・チームによって報告されたTrezorウォレットの”修復不可能”な脆弱性。Trezor社の製品には、ハードウェアウォレットが物理的に盗まれてしまった場合、攻撃者が高度なエンジニアリングの知識を有し、100万円以上もする高価なデバイスを駆使すれば、[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#seed)フレーズが抜かれてしまう可能性があることがそれまでにも知られていたが、今回のこの報告では、身近な電気屋で1万円ほどで手に入る材料と、電子工作の基礎的な知識があれば、誰でも5分以内にシードを抜き取れてしまう方法であったことから大きな波紋を呼んだ。（Ledgerのセキュリティチームは、広範囲への影響を考え、攻撃手法の詳細に関しては非公開としている。）またこの脆弱性はTrezor[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#wallet)のハードウェア設計に起因するため、今後のファームウェア・アップデートなどにより防ぎようがなかったことも、利用者への衝撃をさらに大きくした。Trezor社は、ハードウェアのデザイン上、改善のしようがない問題としてユーザーにも周知しており、この攻撃に対する唯一の防御策として、利用者に「パスフレーズ」の設定を強く推奨する旨の [公式発表](https://blog.trezor.io/our-response-to-ledgers-mitbitcoinexpo-findings-194f1b0a97d4) を行っている。



### Ledger社個人情報データ漏洩事件（2020年12月)


Ledger社の顧客データベースがハッキングされ、同社でハードウェアウォレット注文した人々の100万件の電子メールアドレスと27万2000件の氏名、住所、電話番号が、世界最大のハッカーフォーラム、RaidForumsで暴露された事件。その後、漏洩した個人情報を元に多数のLedgerユーザーに対してフィッシング攻撃やメールによる脅迫などが相次いだ。中にはLedger社のお詫びを装い、同社製品にそっくりな偽物のハードウェアウォレットを送り付けられた事例もある。暗号資産に関わる製品に紐づくユーザーの個人情報の漏洩は、時にユーザーの資産のみならず命をも危険にさらす可能性があることを世に広く知らしめた事件。


これら２つの事件は、ハードウェアウォレットそのもののみならず、それを提供する会社のセキュリティ意識への信頼性をも、ユーザーに深く考えさせる契機となった大きな事件でした。

その点、Coinkite社のセキュリティへの意識とその取り組みは他社を大きく先行しています。例えば、注文時に必要な個人情報の扱いに関しては、法的に保管が必要な120日が経過後、自動的に削除されることを早くから公言していますし、最新モデルのMK4では、多くのハードウェアウォレットにたいてい一つだけ実装されているセキュアエレメント（[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ha/#private_key)が保存されるチップ）が、贅沢にも2つ使われており、外部からの解析攻撃がほぼ不可能な設計になっています。しかもそれぞれあえて違うメーカーのものを搭載し、メーカー固有のバグにも備える徹底ぶりです。

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Starting today customer records will be blanked after 120 days of activity auto-magicaly🧙‍♂️ (i.e. since shipping)<br><br>It&#39;s a very big DB, we don&#39;t want to be marked as spammers so the email notification roll-out will take a couple weeks<br><br>Subject: Protecting Your Privacy: Data Blanked <a href="https://t.co/Rr7mV4nhhr">pic.twitter.com/Rr7mV4nhhr</a></p>&mdash; COLDCARD (@COLDCARDwallet) <a href="https://twitter.com/COLDCARDwallet/status/1341073190815207424?ref_src=twsrc%5Etfw">December 21, 2020</a></blockquote>

> Coinkiteでは、お客様のプライバシーを守るため、顧客情報は自動的にデータベースから削除しています。2020/12/21
>

![](/_images/ColdcardGuide01_4.jpg)

- USB-Cコネクタ
- 無制限メモリ、ビットコイン[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-ta/#transaction)サイズ無制限
- あらゆるデータタイプ、PSBT、[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-a/#address)などがNFCタップで利用可
- スライド式カバーで表示画面を保護
- さらなるセキュリティ：デュアルSE（セキュア・エレメント）
    - 拡張されたデュアレスPIN機能
    - 複数ヴェンダーによるソリューション
- USBヴァーチャルデスクモード


「でもそれだって、企業側が言ってることをそのまま鵜呑みにしてるだけですよね？普段から **”Don’t trust, verify.”（信用するな、検証しろ)** とかカッコいいこと言っておいて、そこはスルーなんすか。そんな日和見でいいんすか！日出る国のジャパニーズビットコイナーさんよぅ！！」

もっともなご意見です。そうですよね。どこの馬の骨ともわからぬ海外企業が生成した秘密鍵何て、そもそも信用できないですよね。本物のビットコイナーなら、自分でちゃんと硬貨を投げて、表が出たら0、裏が出たら1、これを256回繰り返して、自分だけのコールドウォレットを作っているはずですものね。

![](/_images/ColdcardGuide01_5.gif)

ソース：[https://www.youtube.com/watch?v=ieHoQ4sGuEY](https://www.youtube.com/watch?v=ieHoQ4sGuEY)

（数時間後、キャッチしそこね、冷蔵庫下に転がり込んだ硬貨を呆然と見つめながら…）

…すいません、すごく面倒くさいのでそこだけ妥協してもらっても良いでしょうか。人間社会で生きていくなら、これからも我々には最低限のトラストは必要だと思うのです。家族や友人、同じ志を持つほかの人々すら信頼できない社会で、いくら自分だけ富を蓄財したとてそれに一体何の価値がありましょうか。僕らはこれからの人類の未来について、毎回サイコロを振って決めるわけにはいかないのです。何でしたら、Coldcardには、自分でサイコロを100回振って、ハードウェアウォレットのエントロピー(ランダム性)にすら頼らないシードフレーズを生成する機能もありますので、何卒ご容赦ください。

![](/_images/ColdcardGuide01_6.png)

ソース：[https://youtu.be/Rc29d9m92xg](https://youtu.be/Rc29d9m92xg)

> サイコロを振ってユニークなシードを作ることができます。256-bitセキュリティには、少なくとも99回、サイコロを振る必要があります。少ない場合は、警告メッセージが表示されます。
>

正直「自分でサイコロ100回振ってエントロピー作成？なにその機能？いる？そこまでやる？」って思いません？

そうなんです。Coldcardは、ユーザーのセキュリティ＆プライバシー要求に過剰なまでに先回りして応えてくれる業界唯一の製品なんです。もちろん、基本的なセットアップと使い方をするだけなら、[クイックガイド](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcard_beginner_guide/)を読めば一般的なユーザーでも、ものの5分もあればすぐに使い始められます。それとは別に、自身のプライバシーとセキュリティに一切の妥協をしたくないユーザー向けに、その名も[**"パラノイド(偏執病患者向け)ガイド"**](https://coldcard.com/docs/paranoid)が存在しているのがColdcardの面白いところです。

そうしたセキュリティへの先進的な試み、機能はざっと紹介するだけでも


- 梱包袋に特殊な加工が施されており、輸送時の悪意ある攻撃（サプライチェーン攻撃）が検知可能
- インターネットに接続されたPCなどに一度も接続することなく運用可能（エアギャップ機能）
- ハードウェアウォレットの安全性を確実にするパスフレーズが100文字まで設定可能
- Coldcardへのログインを13回連続で失敗すると、デバイスが破壊され二度と使用できなくなる


最後のなんか、自分はいつから007の主人公に？といった趣きのやり過ぎ感すらあります。それでも、彼らがここまでするのは、何よりビットコインを生んだ思想の源流とも言える[サイファーパンク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/glossary-sa/#cypherpunk)的価値観を、ハードウェアウォレットと言うツールを通じてこの世界に体現しようとしているからに他なりません。

![](/_images/ColdcardGuide01_7.jpg)

> プライバシーは、デジタル時代のオープンな社会にとってなくてはならないものである。プライバシーとは秘密主義とは違う。プライベートなことというのは、全世界には知られたくはないことだが、秘密なことというのは誰にも知られたくはないこと。プライバシーとは、自身を世界に向けて選択的に開示できる力のことを言う。 ー エリック・ヒューズ、サイファーパンク宣言(1993)
>

こうした強い思いに基づくてんこ盛りの機能や、何層にもはりめぐらされたセキュリティー対策と扱い方のクセが、Coldcardの使いにくさ＆わかりにくさに繋がり、初心者を露頭に迷わせてしまう原因であるのは否めません。しかし逆に言えば、それら一つ一つを学んで自分のものにしていけば、それはそのまま未来永劫ビットコインを安全に保管するための知識となって、自分の中に蓄積されていきます。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">「私が何度も何度も繰り返し人々にアドバイスしているのは“このテクノロジーの理解に投資しなさいという事”“このテクノロジーのスキルに投資しなさいという事”“このテクノロジーの教育と、知識に投資しなさいという事” なぜなら、それらの価値は週末に40％も下落したりしないからです。」<a href="https://twitter.com/hashtag/BTC?src=hash&amp;ref_src=twsrc%5Etfw">#BTC</a></p>&mdash; aantonop_quotes (@AantonopQuotes) <a href="https://twitter.com/AantonopQuotes/status/1480265733170819077?ref_src=twsrc%5Etfw">January 9, 2022</a></blockquote>

ビットコインはピュアな「情報」に他なりません。それゆえビットコインを正しく「所有する」ということは、ビットコインを正しく「知る」ことに等しいのです。

この記事を読んで興味を持たれた方がもしおられましたら、ぜひこの機会にColdcardという羅針盤を手に、僕と一緒にビットコインのラビットホールを探検してみませんか？


次回は[「Coldcard購入編」](http://lostinbitcoin.jp.testrs.jp/staging/how-to/coldcardguide02/)です。

***
[利用規約 A](http://lostinbitcoin.jp.testrs.jp/staging/copyright/#uaa)
