---
title: ビットコイン鍵管理の心得
taxonomy:
    category:
        - how-to
        - wallet
    post_tag:
        - beginner
---

## ビットコインの自己管理においてすべきこと、してはいけないこと

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインを安全に管理するには  |  ![Tag](/_images/tag.png)  |  初級  | ![Time](/_images/timer.png)  |  16分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

*本記事は  [Casa](https://keys.casa/) の共同創業者＆最高技術責任者 [Jameson Lopp](https://twitter.com/lopp) 氏著「[The dos and don'ts of Bitcoin key management](https://blog.keys.casa/the-dos-and-donts-of-bitcoin-key-management/)」（2020年6月6日公開）を [@akipponn](https://twitter.com/akipponn) さんが翻訳、[@TerukoNeriki](https://twitter.com/TerukoNeriki) が一部加筆修正したものです。*

ビットコインはユーザーに自分の資産に対して非常に高いレベルの主権を提供します。「自分の資産は自分で守れ」（be your own bank）という言い回しを聞いたことがある人もいるかもしれません。これはビットコインが所有者に与える力をうまく表現しています。一方で資産を自ら守るには多大な責任を伴います。ビットコインの価値の源泉とも言える特徴（誰でも自由に参加できるオープンな決済ネットワーク、送金の検閲や資産の押収が困難なことなど）は、悪意のある攻撃者にとっても魅力的なものです。攻撃者はビットコイン所有者を騙して資産を奪うべくさまざまな罠を考案し、ビットコインの安全管理を困難にしています。インターネットは危険な場所です。でもご心配なく。自分の身と資産を守るためのツールはあります！


### **主導権を握ろう**

秘密鍵を自分で管理していなければ、その鍵が本当に安全に保管されているか知る由もありません。たとえ鍵の預け先が暗号通貨取引所など信頼できる第三者だとしても、実際に鍵がどのように管理されているかを監査することはできません。

> [あなたがビットコインを使いこなすスキルを習得する気がないなら、他の誰かがあなたのビットコインを使いこなすことになるでしょう。— Jameson Lopp (@lopp) 2020年5月17日](https://twitter.com/lopp/status/1261849122090283009?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1261849122090283009%7Ctwgr%5E%7Ctwcon%5Es1_c10&ref_url=https%3A%2F%2Fblog.keys.casa%2Fthe-dos-and-donts-of-bitcoin-key-management%2F)

信頼できる第三者に秘密鍵の管理を任せると、秘密鍵管理に付随するリスクから開放されたように感じるかもしれません。でもそれは錯覚です。鍵管理を他者に委託しても、鍵管理に伴う不可避なリスクから逃れることはできません。その上、リスク回避手段を自ら講じることができなくなってしまいます。さらに、以下のような新たな攻撃可能性が生じ、結果的にリスクは増大します。



* ビットコイン管理代行業者が会社ぐるみで顧客資産を横領
* ビットコイン管理代行業者の一部従業員が顧客資産を横領
* 大量のビットコインを管理する代行業者をハッカーが攻撃して顧客資産を横領

本記事は長い上に難解かもしれません。でも「知識は力なり」です。


### **自分の身は自分で守ろう**

所有するすべてのオンラインアカウントについて、サイバー攻撃への強固なセキュリティ対策を講じてください。ユーザーIDとパスワードは遅かれ早かれ漏洩するものだと思ってください。パスワードマネージャ（できれば Yubikey のようなハードウェアタイプの２段階認証を採用するもの）を使って、サービスごとに異なるパスワードを設定してください。２段階認証に対応しているサービスでは、必ず有効にしてください（ハードウェアタイプの２段階認証を推奨）。TOTP（Time-based One-time Password、時間に基づいて生成されるワンタイムパスワード）にしか対応していないサービスの場合、[Yubico Authenticator](https://support.yubico.com/support/solutions/articles/15000006419-using-your-yubikey-with-authenticator-codes) を使えばハードウェア（Yubikey）で保護できます。

サイバーセキュリティや運用セキュリティに馴染みのない方は「[Jolly Roger’s Security Thread for Beginners](https://www.lopp.net/pdf/Jolly_Rogers_Security_Guide_for_Beginners.pdf)」（Jolly Rogerの初心者のためのセキュリティスレッド）をぜひ読んでみてください。

秘密鍵の管理については、利便性とセキュリティはトレードオフの関係にあること覚えておいてください。スマートフォンのシングルシグ（送金に１つの秘密鍵による署名しか要しない）ウォレットアプリは日常使いの少額のビットコインを保管するには便利ですが、老後の蓄えの保管に使ってはいけません。一方、マルチシグ（送金に複数の秘密鍵による署名が必要）ウォレットの秘密鍵を地理的に分散保管する場合、送金手順が煩雑になるため日常使いには不便ですが、送金頻度が月１回または年１回と少なければ問題ないでしょう。

秘密鍵の保管には専用のハードウェアを使い、送金先アドレスは必ずハードウェアの画面で確認しましょう。[PCやスマホのアプリ、ブラウザに表示されるアドレス](https://techcrunch.com/2018/07/03/new-malware-highjacks-your-windows-clipboard-to-change-crypto-addresses/)は改ざんされる可能性があるため、信用してはいけません。

送金先アドレスは最初の数文字だけでなく、全ての文字列をチェックしてください。送金先アドレスに類似するアドレスを生成して、本来の送金先とすり替えてビットコインを騙し取ろうとするマルウェアが数多く報告されています。 

> [クリップボードのデータを改ざんして暗号通貨の盗難を試みるマルウェア ComboJack｜ZDNet](https://www.zdnet.com/article/exclusive-google-removes-49-chrome-extensions-caught-stealing-crypto-wallet-keys/)

災害にもしっかり備えてください。ウォレットを復元するために必要なシードフレーズのバックアップ方法を考える必要があるかもしれません。シードフレーズの保管については[さまざまなガイド](https://www.lopp.net/bitcoin-information/security.html)が公開されているので参考にしてください。弊社Casaでは、顧客はシードフレーズを管理すべきでないとの考えに基づいてサービスを提供しています。その理由は以下の記事で説明しています。 

> [Casa のシードフレーズに頼らないセキュリティモデル](https://blog.keys.casa/casa-seedless-security-model/)

金属製デバイスにシードフレーズのバックアップを保存する場合、ストレステストを通過した極限状態に耐えられることが証明されたものを購入してください。 

> [ビットコインのシードフレーズ保管用金属製デバイスの評価](https://jlopp.github.io/metal-bitcoin-storage-reviews/)

新たにソフトウェアをインストールする場合、それが[悪意ある偽物](https://www.reddit.com/r/Bitcoin/comments/g3rsaz/just_another_psa_if_you_search_on_the_chrome_web/)ではないか検証してください。残念ながら、検証方法はプラットフォームによってまちまちです。パソコンにインストールするソフトウェアについては、コマンドラインが使える人なら GPG 署名を検証できます。モバイルアプリは暗号学的署名がされていますが、この署名の正当性は App Store や Google Play などアプリストアでしか検証できません。偽物をインストールしないために、アプリ開発会社の公式ウェブサイトからダウンロードしてください。


#### **フィッシング詐欺の被害にあわないために**

インターネットに接続しているコンピュータやスマートフォン、特にウェブブラウザには決してシードフレーズを入力しないこと！専用ハードウェアで秘密鍵を保管する人が増えた今、ハッカーが狙っているのはハードウェアウォレット所有者です。

![](/_images/the_dos_and_don'ts_of_bitcoin_key_management_1.jpeg)


あまり知られていない攻撃手法に**タイポスクワッティング**があります。ハッカーはビットコイン所有者がビットコイン関連サービスサイトにアクセスする際にURLのタイプミスでアクセスしそうなドメインを購入し、獲物を待ちます。こうした悪意ある偽サイトに誤ってアクセスするのを防ぐため、金融関連サービスのウェブサイトはあらかじめブックマークしておき、常にブックマークからアクセスしましょう。

> [2,400万ユーロ相当の暗号通貨を盗んだ疑いでイギリスとオランダで６人が逮捕](https://www.europol.europa.eu/newsroom/news/6-arrested-in-uk-and-netherlands-in-%E2%82%AC24-million-cryptocurrency-theft)

タイポスクワッティングについて調査中、興味深いサイトを発見しました。オランダの取引所 [Bitonic](https://bitonic.nl/) がタイポスクワッティングについて注意喚起するために開設した [http://bitadress.org/](http://bitadress.org/) です。

タイポスクワッティングと似た攻撃に、検索エンジンに広告料を支払って悪意ある偽サイトを正規サイトより上位に表示させる手法があります。正規サイトよりも先に表示される偽サイトに誘導してビットコインを盗もうとするものです。これは前述のウェブサイトへのアクセスをブックマーク経由に限定する方法で回避できます

![](/_images/the_dos_and_don'ts_of_bitcoin_key_management_2.png)



#### **マルウェアをインストールしない**

ブラウザの拡張機能を安易にインストールしないでください。[悪意のあるもの](https://medium.com/mycrypto/discovering-fake-browser-extensions-that-target-users-of-ledger-trezor-mew-metamask-and-more-e281a2b80ff9)もあり、ウェブサイトの閲覧履歴を収集されてしまうかもしれません。

> [独占スクープ： Googleが暗号通貨ウォレットの秘密鍵を盗む49の Chrome 拡張機能を削除｜ZDNet](https://www.zdnet.com/article/exclusive-google-removes-49-chrome-extensions-caught-stealing-crypto-wallet-keys/)

ブラウザ拡張機能タイプのウォレットは[あからさまな詐欺の可能性がある](https://www.crowdfundinsider.com/2020/01/155894-another-malicious-crypto-wallet-app-stealing-private-keys-and-data/)ので使わないでください。

ソフトウェアが多数インストールされたパソコンにウォレットアプリをインストールするのは避けましょう。ウォレット以外のソフトウェアにクリップボードのデータを改ざんするマルウェアやパソコンに保存された[秘密鍵を探す](https://snyk.io/blog/malicious-code-found-in-npm-package-event-stream/)トロイの木馬を[仕込まれる危険性](https://blog.reversinglabs.com/blog/mining-for-malicious-ruby-gems)が高まります。

[ハードドライブを乗っ取るランサムウェア](https://www.technologyreview.com/2018/04/19/104453/true-scale-of-bitcoin-ransomware-extortion-revealed/)に気をつけてください。ソフトウェアは海賊版を避けて正規版だけをインストールしましょう。万が一、乗っ取られてもデータを復元できるよう[定期的にハードドライブのバックアップ](https://blog.lopp.net/how-to-securely-back-up-data-to-cloud-storage/)をとってください。

QR コードを生成するサイト、特に「ビットコイン QR コードジェネレータ」は利用しないでください。あなたのアドレスが攻撃者のアドレスに改ざんされる可能性があります。

> [ビットコインアドレスを QR コードに変換するというこのサイト、何を入力してもサイト運営者のアドレスを出力する。 詐欺サイト以外の何者でもない。](https://www.reddit.com/r/Bitcoin/comments/gtr2p4/this_website_claims_to_turn_your_addresseinto_a/?ref=share&ref_source=embed&utm_content=media&utm_medium=post_embed&utm_name=24092cb1606a4f2fb8b2cfbefc02e560&utm_source=embedly&utm_term=gtr2p4)
> 
> ![](/_images/the_dos_and_don'ts_of_bitcoin_key_management_3.jpeg)

可能なら、ソフトウェアはインストール前に正規版かどうか検証、つまり、ダウンロードしたバイナリのファイルハッシュと GPG 署名を確認しましょう。秘密鍵を管理するソフトウェアについては、例えば、サードパーティが管理するAWSイメージを実行するなど動作検証が不可能な場合、インストールを見合わせてください。

> [ビットコインコアノードがハックされました](https://www.reddit.com/r/Bitcoin/comments/jrxgj8/bitcoin_core_node_hacked/?ref=share&ref_source=embed&utm_content=title&utm_medium=post_embed&utm_name=8783fde0e481492686bb852ac7bdbe77&utm_source=embedly&utm_term=jrxgj8)


#### **技術的脆弱性を作らない**

秘密鍵のバックアップをデジタルデータとして保存すること、特にクラウドなどオンラインサービスを利用することは避けるべきです。安全にデジタルバックアップを作ることは可能ですが、技術やセキュリティについての専門知識を要します。

> [暗号通貨ユーチューバー、ライブ配信中に200万ドル相当の暗号通貨を盗まれたと主張](https://gizmodo.com/2-million-allegedly-stolen-from-cryptocurrency-vlogger-1825290362)

ブラウザベースのウォレットは、ハードウェアウォレットの単なるインターフェースであっても利用は避けるべきです。ブラウザにはさまざまな脆弱性があります。

> [ブラウザベースのビットコインウォレットが抱えるセキュリティ問題](https://blog.keys.casa/security-issues-with-browser-based-bitcoin-wallets/)

Tor ブラウザを使ってビットコインの送金先アドレスを表示するウェブサイトにアクセスしている人は、悪意ある Tor リレーノードが送金先アドレスを改ざんする可能性があることを認識しておくべきです。

> [2020年版 悪意ある Tor リレーノードによるユーザ攻撃実例（パート１）](https://medium.com/@nusenu/how-malicious-tor-relays-are-exploiting-users-in-2020-part-i-1097575c0cac)

ブレインウォレット（秘密鍵やシードフレーズを暗記すること）は避けてください。人間はエントロピー生成が苦手です。よく使う英単語を並べたシードフレーズで復元できるブレインウォレットに送金したビットコインは、数秒後には盗まれてしまうでしょう。

<center>DEF CON 23 - Ryan Castellucci - ブレインウォレットをハックする</center>
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/foil0hzl4Pg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>

シャミアの秘密分散法には以下ブログ記事で詳しく説明した通り、欠点が多いため使わないでください。

> [シャミアの秘密分散法の欠点](https://blog.keys.casa/shamirs-secret-sharing-security-shortcomings/)

シードフレーズを分割して分散保管するのは避けてください。総当たり攻撃への耐性が大幅に低下します。

<center>ビットコイン Q&A： シードフレーズを分割してはいけない理由</center>
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/p5nSibpfHYE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>

シードフレーズのバックアップに創造性は不要です。独自に考案したバックアップ方法は総じて安全性が低く、ウォレットを復元できなくなるリスクがあります。具体的なリスクについては以下記事をご参照ください。

> [ビットコインのシードフレーズの安全な管理法](https://blog.keys.casa/bitcoin-seed-security-analysis/)

同様に、シードフレーズのバックアップのランダム化も無意味です。シードフレーズにはチェックサムが含まれるため、シードフレーズの長さによっては総当たり攻撃で割り出すのは簡単です。12の英単語からなるシードフレーズの組み合わせはたったの５億通りしかなく、その中で有効な組み合わせはおそらく５万通りほどです。有能なハッカーなら、わずか数分で５万通りの組み合わせを試してビットコインを盗めます。

ペーパーウォレットは使わないでください。ペーパーウォレットを安全に使うのは難しく、付随するリスクを十分に理解していないとビットコインを誤って失うことになるでしょう。 

<center>ビットコイン Q&A： ペーパーウォレットのメリットとデメリット</center>
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/cKehFazo8Pw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>

弊社 Casa の新規顧客の共通点に、ハードウェアウォレットやペーパーウォレットなど複数のシングルシグウォレットにビットコインを分散保管していることがあります。これはビットコインを全て失うという致命的リスクを下げるものの、一部を失うリスクを高めます。_単一障害点を持つ複数のウォレットに秘密鍵を分散保管しても安全性は向上しません。_


#### **詐欺に引っかからない**

スケアウェアや脅迫メールのメッセージを信じないでください。実際に使用しているユーザー名やパスワードが含まれていたりすると慌ててしまうと思いますが、それらはオンラインサービス事業者のデータベースから漏洩してダークウェブで売買されているものです。本記事執筆時点において、この種の詐欺の最新バージョンは「セクストーション（性的脅迫）詐欺」と呼ばれるもので、あなたのコンピュータをマルウェアに感染させ、恥ずかしい性的画像を撮影したと脅してきます。

「Xビットコインを送金すれば2Xビットコインがもらえる」と喧伝する詐欺は未だに健在です。あなたのビットコインを数分だけ預かって、そのお礼にビットコインを倍返しする人などいません。貨幣の時間的価値はそんなに高くないです。

> [ビル・ゲイツ、イーロン・マスク、ジャック・ドーシーといった著名人がビットコインをばらまくことはありません。２倍３倍にして返すという人にビットコインを送ったら、間違いなく何も返ってきません。私が保証します。— Jameson Lopp (@lopp) 2020年4月24日](https://twitter.com/lopp/status/1253660099089960961?ref_src=twsrc%5Etfw)

エアドロップされるアルトコインを集めようとしてはいけません。[詐欺の可能性](https://blessedreams.wordpress.com/2020/05/02/beware-of-fake-blockchain-airdrops-offers/)があります。ホットウォレットやオンラインサービスのログイン情報を盗むことが目的かもしれません。より高度な詐欺にビットコインを盗むマルウェアが仕込まれたウォレットがあります。エアドロップされるフォークコインをウォレットで安全に受け取る方法は、エアドロップ前にウォレットで管理するビットコインを全て別の新しいウォレットに送金することです。

> [ビットコインゴールドのウォレット詐欺、被害額は300万ドル相当 - CoinDesk](https://www.coindesk.com/bitcoin-gold-wallet-scam-nets-3-million-illicit-earnings)

ビットコインをミキシングサイトに送らないでください。大半は詐欺サイトです。ミキシングを安全に行うには、自分でミキシングソフトウェアを実行し、秘密鍵の管理権限を放棄しないことです。これが可能なミキシングソフトウェアとして [JoinMarket](https://github.com/JoinMarket-Org/joinmarket-clientserver)、[Wasabi](https://wasabiwallet.io/)、[Whirlpool](https://samouraiwallet.com/whirlpool) などがあります。

> [ビットコインの取引や送金を最近始めたばかりです。よく調べずにビットコインをミキシングサイトに送金ししたところ、151承認後の今も送金したビットコインがサイトに反映されません。](https://www.reddit.com/r/Bitcoin/comments/geecug/recently_got_into_trading_and_sending_bitcoin)

十分な調査を行わないでICOに投資するのはやめましょう。[ブルームバーグの調査レポート](https://research.bloomberg.com/pub/res/d28giW28tf6G7T_Wr77aU0gDgFQ)によると、ICOの８割が詐欺です。

同様に、欲にかられて「パンプ＆ダンプ（価格操作）」グループに参加しないでください。このようなグループでは、利益を得るのは少数のインサイダーだけで、あなたは資金を失うことになります。

> [詐欺師がフェイクニュースでビットコイン投資家を騙す手口](https://www.buzzfeednews.com/article/ryanmac/heres-how-scammers-are-using-fake-news-to-screw-with-bitcoin)

ハードウェアウォレットを転売業者から買わないでください。また第三者から提供されたシードフレーズでハードウォレットを初期化しないでください。

> [中古の Ledger ハードウェアウォレットから盗まれた老後の備え](https://cointelegraph.com/news/life-savings-stolen-from-second-hand-ledger-hardware-wallet)


#### **ハッキング被害に合わない**

Teamviewer のようなリモートアクセスソフトウェアを決してインストールしないでください。

> [ハッキングされて 40.5 BTC を失いました。絶望しています。犯人探しを手伝ってください。](https://www.reddit.com/r/Bitcoin/comments/2og50r/im_devastated_got_hacked_and_lost_405_btcs_please)


#### **攻撃の標的にならない**

所有するビットコインについて話をすると攻撃の標的にされる可能性があります。以下で Cody は Coinbase アカウントをハッキングされた友人についてツイートしていますが、同時に Cody 自身も Coinbase に資金を預けていることを暴露しています。

> [@adachis の身に起きたことは、 @coinbase にとってかなり厄介です。私もビットコイン取引はすべて Coinbase で行っているので、Coinbase の透明性の欠如と対応に不安を感じています。— codyb (@codybrown) 2017年5月21日](https://twitter.com/codybrown/status/866442341946675200?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E866442341946675200%7Ctwgr%5E%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fblog.keys.casa%2Fthe-dos-and-donts-of-bitcoin-key-management%2F)

このツイートから数日後、Cody は SIM スワップ攻撃を受け、友人同様、Coinbase 口座から資金を盗まれてしまいました。

> [VerizonとCoinbaseのせいで、15分間のうちに8,000ドル相当のビットコインを喪失した経緯](https://medium.com/@CodyBrown/how-to-lose-8k-worth-of-bitcoin-in-15-minutes-with-verizon-and-coinbase-com-ba75fb8d0bac)

電話番号とオンラインアカウントを決して紐づけないでください。攻撃者はあなたの電話番号に対して SIM スワップ攻撃をしかけ、あなたの電話番号に紐づいたアカウントのパスワードをリセットし、アカウントを乗っ取ります。今や定番手口となり頻発する攻撃です。私は BitGo で働いていた時にこの手口をいち早く察知し、[プラットフォームから SMS を使った認証機能を削除しました](https://blog.bitgo.com/bitgo-phasing-out-sms-based-2-factor-authentication-96db16fdd63a)。それから３年後、 BitGo のエンジニアの一人が Coinbase でこの脆弱性の犠牲になりました。

> [人生で最も高価な教訓： SIM ポートハックの詳細](https://medium.com/coinmonks/the-most-expensive-lesson-of-my-life-details-of-sim-port-hack-35de11517124)


### **セキュリティは常に進化しています**

攻撃する側と防御する側の戦いは、双方が新しい戦術を編み出し、相手の出方をうかがいながら常に進化しています。

あなたのビットコインに迫る脅威の大きさに圧倒されたかもしれません。でも恐れる必要はありません。弊社 Casa のビットコイン自己管理ソリューションなら、あなたのビットコインに迫る脅威を軽減できます。

*訳者注）Casa はマルチシグによるジョイントカストディ・サービスを提供するアメリカの企業です。本記事は Casa のサービス利用を推奨するものではありません。
*


### 著作権等について
[利用規約 A](https://lostinbitcoin.jp/copyright/#uaa)
