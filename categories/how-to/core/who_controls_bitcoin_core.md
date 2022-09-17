---
title: Bitcoin Core のプロジェクトマネージャーは誰？
taxonomy:
    category:
        - how-to
        - core
    post_tag:
        - beginner
---

## ビットコインの開発現場は誰がどのように運営管理しているのか？

|  ![Category](/_images/category.png)  |  ハウツー、ビットコインコア開発に参加するには  |  ![Tag](/_images/tag.png)  |  初級  | ![Time](/_images/timer.png)  |  17分  |
| ---- | ---- | ---- | ---- | ---- | ---- |

_本記事は [Casa](https://keys.casa/) の共同創設者＆最高技術責任者　[JAMESON LOPP](https://twitter.com/lopp) 氏著「 [Who Controls Bitcoin Core?](https://blog.lopp.net/who-controls-bitcoin-core-/) 」（2018年12月15日公開）を [Katakoto](https://twitter.com/katakoto) さんが翻訳、[@TerukoNeriki](https://twitter.com/TerukoNeriki)  が一部加筆修正したものです。_



[Bitcoin Core](https://bitcoincore.org/) の [GitHub](https://github.com/bitcoin/bitcoin) リポジトリにコード変更をマージする権限は一体誰が持っているのか？これは非常によくある質問です。長年、関係者の間では、マージ権限がビットコインプロトコルの「管理中枢」とされてきました。しかし、私はこの質問自体が権威主義的で的外れだと考えます。私の主張に賛同する人は少ないでしょう。そこで本記事では、 Bitcoin Core の開発現場、さらにはビットコインプロトコルの進化過程を解説します。


### Bitcoin Core の歴史

Bitcoin Core はビットコインプロトコル開発の指揮中枢と言うよりは、[フォーカルポイント](https://en.wikipedia.org/wiki/Focal_point_%28game_theory%29)（ゲーム理論でプレイヤーが相互にコミュニケーションをとれない場合にデフォルトで選択される傾向があるソリューション）です。もし何らかの理由で Bitcoin Core が消滅しても、新たなフォーカルポイントが生まれるでしょう。現在は GitHub リポジトリが技術議論のプラットフォームとしてプロトコル開発拠点となっていますが、コミュニケーションプラットフォームは利便性の問題であり、プロジェクトの定義や整合性とは無関係です。実際、ビットコイン開発のフォーカルポイントは、プラットフォームだけでなく、その名前さえも変化してきたのです。



* 2009年初頭、ビットコインプロジェクトのソースコードは SourceForge に保存された[ただの .rar ファイル](https://www.metzdowd.com/pipermail/cryptography/2009-January/014994.html)でした。サトシと初期開発者たちはコードパッチを[電子メールで](https://online.wsj.com/public/resources/documents/finneynakamotoemails.pdf)送受信していました。
* 2009年10月30日、 Sirius （ [Martti Malmi](https://mmalmi.medium.com/) ）が SourceForge にビットコインプロジェクトのために [Subversion リポジトリを作成](https://sourceforge.net/p/bitcoin/code/1/)しました。
* 2011年、ビットコインプロジェクトは [SourceForge](https://sourceforge.net/p/bitcoin/code/252) から [GitHub ](https://github.com/bitcoin/bitcoin/commit/ca40e581ebcdc85dba15c1e873f5e5aedda45b77)に移行。
* 2014年、ビットコインプロジェクトは [Bitcoin Core に改名](https://github.com/bitcoin/bitcoin/pull/3408)されました。


### 誰も信用しない

GitHub には Organization レベルの「メンテナー」アカウントが複数あります。メインテナーはマスターブランチにコードをマージできます。メインテナーは特権的立場というよりは、保守管理機能に近いです。もし誰でも自由にマスターブランチにマージできるとしたら、すぐに「船頭多くして船山に登る」状況に陥ることは目に見えています。 Bitcoin Core は個人に与えられた権力が乱用された場合、容易にそれを覆せるという「最小特権の原則」に従っています。

> Core はマージコミットへの署名が可能な PGP 鍵という重要リストに関して透明性を保っています。
> 
> ここで学ぶべきは GitHub を信用してはいけないということです！ Bitcoin Core でさえ、リポジトリの変更権限を持つ人物を全員把握しているわけではありません。おそらく GitHub 従業員だけでも数十人がその権限を持つでしょう。
> 
> [Peter Todd](https://twitter.com/peterktodd/status/1047854713029312512)（2018年10月4日）

敵対的アプローチをとるなら、GitHub は信用できません。GitHub の従業員は管理者権限を使って、メンテナーの同意なしにリポジトリに悪意あるコードを追加することができます。しかしながら、 GitHub 従業員が Bitcoin Core メンテナーの PGP 鍵を不正入手する可能性は限られています。 Bitcoin Core はコードの整合性を GitHub アカウントではなく、すべてのマージコミットが信頼できる PGP 鍵で署名されていることを確認するという継続的な統合システムに委ねています。PGP 鍵は既知のIDと紐づいていますが、常にそうであると仮定するのは危険です。なぜなら鍵が漏洩しても、鍵保有者が他のメンテナーに通知しない限り、漏洩事実を知る術がないからです。このように、コミットに署名する PGP 鍵は完璧なセキュリティを保証するものではありません。攻撃者による不正なコードの追加を困難にするだけです。


### 王国への鍵

執筆時点で[信頼できる PGP フィンガープリント](https://github.com/bitcoin/bitcoin/blob/master/contrib/verify-commits/trusted-keys)は以下の通りです。

> 71A3B16735405025D447E8F274810B012346C9A6
> 133EAC179436F14A5CF1B794860FEB804E669320
> 32EE5C4C3FA15CCADB46ABE529D4BCB6416F53EC
> B8B3F1C0E58C15DB6A81D30C3648A882F4316B9B
> CA03882CB1FC067B5D3ACFE4D300116E1C875A3D

上記の鍵は、以下５名のものとされています。

> Wladimir J. van der Laan &lt;[laanwj@protonmail.com](mailto:laanwj@protonmail.com)>
> 
> Pieter Wuille &lt;[pieter.wuille@gmail.com](mailto:pieter.wuille@gmail.com)>
> 
> Jonas Schnelli &lt;[dev@jonasschnelli.ch](mailto:dev@jonasschnelli.ch)>
> 
> Marco Falke &lt;[marco.falke@tum.de](mailto:marco.falke@tum.de)>
> 
> Samuel Dobson &lt;[dobsonsa68@gmail.com](mailto:dobsonsa68@gmail.com)>

これは私たちがこの５人を信用しているということを意味するのでしょうか？必ずしもそうではありません。鍵は身分証明書ではないですし、鍵が誰か他の人の手に渡る可能性もあります。では、検証用の verify-commits という Python スクリプトを実行することで得られる保証とは一体何でしょうか？

> python3 contrib/verify-commits/verify-commits.py
> 
> Using verify-commits data from bitcoin/contrib/verify-commits
> 
> All Tree-SHA512s matched up to 309bf16257b2395ce502017be627186b749ee749
> 
> There is a valid path from “HEAD” to 82bcf405f6db1d55b684a1f63a4aabad376cdad7 where all commits are signed!

[verify-commits](https://github.com/bitcoin/bitcoin/tree/master/contrib/verify-commits) スクリプトを使えば、誰でも自分のコンピュータで Bitcoin Core のコードの整合性を確認できます。スクリプトを実行すると、2015年12月のコミット 82bcf405...以降のすべてのマージコミット（執筆時点で3,400以上のマージ）の PGP 署名をチェックし、スクリプトが正常に完了すると、2015年12月以降に変更されたコードのすべての行について、 Bitcoin Core の開発プロセスを経てメンテナー鍵を持つ誰かによって「サインオフ」されたことが示されます。これは悪意あるコードが紛れ込んでいないことを100%保証するものではありませんが（メンテナーが不正を働いたり、鍵を盗まれる可能性もあるため）、攻撃リスクを大幅に下げます。ではメンテナーとは何なのでしょうか？メンテナーになる方法は？これは後ほど説明します。


### 重層的なセキュリティ

Bitcoin Core のコードの整合性は暗号鍵のみに依存するわけではなく、他にもさまざまなチェック機能が働いています。何層にもなるセキュリティのおかげで高い防衛力を維持できるのです。


#### プルリクエストのセキュリティ

1. [bitcoin/bitcoin](https://github.com/bitcoin/bitcoin) のマスターブランチにプルリクエストを送ることで、誰でも自由にソフトウェアを改善するコード変更を提案できます。
2. プルリクエストは他の開発者がレビューし、有害でないことを確認します。プルリクエストのレビューやフィードバック提供は誰でも自由にできます。 Bitcoin Core に貢献するのに試験はありませんし、ゲートキーパーもいませんから。プルリクエストのマージに対して合理的反論がなくなると、メンテナーによってマージされます。
3. コアメンテナーは未署名コミットがリポジトリにプッシュされるのを防ぐため、[プッシュ前のフック](https://github.com/bitcoin/bitcoin/blob/master/contrib/verify-commits/pre-push-hook.sh)を設定します。
4. マージコミットに [OpenTimestamps を使って](https://github.com/bitcoin/bitcoin/blob/ebd786b72a2a15143d7ef4ea2229fef121bd8f12/contrib/devtools/README.md#create-and-verify-timestamps-of-merge-commits)安全にタイムスタンプを打つことも可能です。
5. [Travis CI （Travis 継続的統合）システム](https://travis-ci.org/github/bitcoin/bitcoin)は、 Git ツリー（履歴）の整合性をチェックし、マスターブランチのすべてのコミットに信頼できる PGP 鍵の署名があるかを確認するために、[このスクリプト](https://github.com/bitcoin/bitcoin/blob/master/.travis/lint_06_script.sh)を定期的に実行します。
6. [このスクリプト](https://github.com/bitcoin/bitcoin/blob/master/contrib/verify-commits/verify-commits.py)は誰でも実行可能で、2015年12月以降の全マージコミットの PGP 署名を検証できます。この記事の執筆中、私も自分のノートパソコンで実行してみたところ、検証は25分で完了しました。


#### リリースのセキュリティ

1. [Gitian](https://gitian.org/) の決定論的ビルドシステムでは、同一バイナリの作成を目的として、複数の開発者が各々個別にソースコードをビルドします。もし他の開発者のものと一致しないものをビルドした開発者がいれば、非決定性の発生を意味するので、最終的なリリースは見送られます。非決定性が生じた場合、開発者は問題を突き止めて修正し、別のリリース候補をビルドします。決定論的ビルドが成功したら、開発者はバイナリに署名して、そのバイナリとツールチェーンは改ざんされていないことと、同じソースが使用されていることを保証します。この方法により、ビルドと配布プロセスが単一障害点となるのを防ぎます。技術的スキルがあれば、誰でも自身のビルドシステムを実行できます。[手順についてはこのリンクをご参照ください](https://github.com/bitcoin-core/docs/blob/38befdf71ba21e69a598e974f7c06a9cdb5b0dfd/gitian-building.md)。
2. Gitian ビルドが正常に完了し、ビルダーが署名すると、Bitcoin Core のメンテナーが各ビルドの SHA256 ハッシュを使ってメッセージに PGP 署名します。ビルド済みバイナリを実行する際、ダウンロード後にハッシュを確認することで、署名されたリリースメッセージが本物かどうか検証できます。そのための手順は[こちらをご参照ください](https://bitcoincore.org/en/download/)。
3. 上記はすべてオープンソースなので、スキルと意欲さえあれば誰でも監査が可能です。
4. 上記の品質および整合性チェックをすべて通過すると、 Bitcoin Core にコミットされて最終的にリリース版となるコードはネットワークを構成するノードにデプロイされます。デプロイする主体は中央集権的組織ではなく、ノード運用者です。ノード運用者はノードが実行するコードを更新するかどうか、各自判断しなければなりません。 **Bitcoin Core は意図的に自動更新機能を提供していません。ユーザーが明示的に選択していないコードを実行するのを防ぐためです。**

Bitcoin Core プロジェクトは、こうした数々の技術的なセキュリティ対策を講じていますが、対策はどれも完璧ではなく、理論的には攻撃は可能です。Bitcoin Core のコード整合性の最後の砦は、他のオープンソースプロジェクトと同様、常時警戒体制です。 Bitcoin Core のコードをレビューする人が多ければ多いほど、悪意や欠陥のあるコードのリリース可能性は下がります。


### コードカバレッジ

Bitcoin Core にはテストコードが多数用意されており、すべてのプルリクエストに対して実行される統合テストスイートとマスター上で毎晩実行される拡張テストスイートがあります。

テストのコードカバレッジは、以下の方法で確認できます。

1. Bitcoin Core GitHub リポジトリをクローン
2. ソースからビルドに[必要な依存関係](https://github.com/bitcoin/bitcoin/tree/master/doc#building)をインストール
3. [これらのコマンド](https://github.com/bitcoin/bitcoin/blob/master/doc/developer-notes.md#compiling-for-test-coverage)を実行
4. ./total_coverage/index.html にあるレポートを表示

または Marco Flake がホストしているカバレッジレポートを[こちら](https://marcofalke.github.io/btc_cov/test_bitcoin.coverage/index.html)から確認できます。

![](/_images/who_controls_bitcoin_core_2.png)

コードカバレッジ・レポート

テストカバレッジの広さは、コードが意図通りに動く確実性の高さを意味します。

コンセンサスが肝となるソフトウェアにとって、テストは非常に重要です。特に複雑な変更に際しては、綿密なミューテーションテスト、すなわち、意図的にコードを破壊して想定通りにテストが失敗するかをテストします。 Greb Maxwell は、0.15バージョンのリリース時の議論で、このプロセスについて以下のように述べています。

「テストとはソフトウェアのテストです。ではテストのテストとは？テストをテストするには、ソフトウェアを壊さなければなりません。」—  Greg Maxwell 

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/nSRoEeqYtJA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>


### 自由な市場競争

BitMEX がビットコイン実装のエコシステムについて[素晴らしい記事](https://blog.bitmex.com/bitcoin-cores-competition/)を書いています。ビットコインと互換性のある実装は十数種類あり、「競合ネットワーク」の実装はさらに多いです。これこそオープンソースが実現する自由です。Bitcoin Core プロジェクトに不満があれば、誰でも自由に新たなプロジェクトを始められます。ゼロから作ってもよいですし、 Bitcoin Core のソフトウェアをフォークしてもよいのです。

本記事執筆時点で、アクセス可能なビットコインノードの96％は Bitcoin Core のいずれかのバージョンを実行しています。なぜ Bitcoin Core がここまで優勢なのでしょうか？他の実装への乗り換えコストがゼロに近い場合、Bitcoin Core が独占的地位を維持できる理由は何でしょう？答えは、他の実装も結局はその大半が Bitcoin Core と互換性があるか、少なくとも Bitcoin Core に非常に類似した RPC API を提供しているからです。

![](/_images/who_controls_bitcoin_core_1.png)

これは Bitcoin Core が開発のフォーカルポイントであることの証明だと私は考えています。 Bitcoin Core は他の実装と比べて開発者のレベルの高さと数の多さが桁違いなため、Bitcoin Core のソフトウェアはパフォーマンス、堅牢性、安全性が最も高い傾向にあります。ノード運用者は大切なお金を管理するのに、わざわざ２番目に優れたソフトウェアを選ばないでしょう。またビットコインはコンセンサスソフトウェアであり、ビットコインプロトコルには公式仕様が存在しません（この点についてのコンセンサスはないですが）。なぜなら仕様を決める権限を持つ人がいないからです。こうした状況では、フォーカルポイントの実装を選ぶ方が安全です。バグまで含めて他のネットワーク参加ノードと互換性を保てる可能性が高いためです。この意味において、開発フォーカルポイントのコードは実質的に公式仕様に最も近いと言えます。


### Core 開発者とは？

[Bitcoin Core の開発プロセス](https://github.com/bitcoin/bitcoin/blob/master/CONTRIBUTING.md)に馴染みのない人が外から見ると、プロジェクトチームは一枚岩に見えるかもしれませんが、実際にはそんなことはありません。Core 開発コントリビューター（貢献者）間の意見の対立は日常茶飯事で、[既に多大な貢献をしているベテランのコントリビューター](https://github.com/bitcoin/bitcoin/pulls?utf8=%E2%9C%93&q=is%3Aclosed+is%3Aunmerged+is%3Apr+author%3Asipa+)でさえ、マージされずに終わったコードをたくさん書いています。コントリビューターのためのガイドラインを読むと、かなり緩いことに気が付くでしょう。コントリビューションプロセスは、まさに「[ラフな合意](https://datatracker.ietf.org/doc/html/rfc7282)」と呼ぶにふさわしいかもしれません。

「メンテナーはパッチがプロジェクトの一般原則に沿っているか、マージ要件を満たしているかを考慮し、コントリビューターの全体的な合意を判定します。」

Bitcoin Core のメンテナーとは誰でしょう？一定期間、コンスタントに質の高いアウトプットを出すことで、プロジェクト内で社会資本を築き上げたコントリビューターがメンテナーになります。既存メンテナーたちが、特定分野で能力、信頼性、モチベーションを証明したコントリビューターをメンテナーに加えることが利益に叶うと思えば、その人の GitHub アカウントにコミットアクセスを許可します。リードメンテナーはプロジェクトのあらゆる面における監督者であり、リリース調整の責任者です。リードメンテナーは前任者が自発的に後任者に託す形で交代してきました。以下、これまでと現在のリードメンテナーです。



* Satoshi Nakamoto: 2009年１月３日 ～ [2011年2月23日](https://sourceforge.net/p/bitcoin/mailman/message/27102906/)
* [Gavin Andresen](https://medium.com/@gavinandresen): [2011年2月23日](https://sourceforge.net/p/bitcoin/mailman/message/27102906/) ～ [2014年4月7日](https://bitcoinfoundation.org/bitcoin-core-maintainer-wladimir-van-der-laan/)
* [Wladimir](https://medium.com/@orionwl) van der Laan: [2014年7月14日](https://bitcoinfoundation.org/bitcoin-core-maintainer-wladimir-van-der-laan/) ～ 現在

Bitcoin Core のメンテナーは、しばしば清掃員と呼ばれます。メンテナーはコントリビューターやユーザーの合意を覆すような大きな権限は与えられていないにも関わらず、過剰な注目を集めるなど負担が大きいからです。例えば、Gregory Maxwell は2017年に[個人的な理由](https://www.reddit.com/r/Bitcoin/comments/3x7mrr/gmaxwell_unullc_no_longer_a_bitcoin_committer_on/cy29vkx/)からメンテナーを退任しましたが、一因としてスケーリング議論中に経験したプレッシャーがあると考えられます。Wladimir は Core メンテナーのストレスと、エコシステムに動揺を招いた Gavin のコミットアクセス権の削除が正しい判断だった理由について[示唆に富む投稿](https://laanwj.github.io/2016/05/06/hostility-scams-and-moving-forward.html)をしています。

同様に [Jeff Garzik](https://medium.com/@jgarzik) が GitHub の Organization アカウントから削除された際には、本人も含め憤慨した人が大勢いましたが、Jeff はその時点で[ Core には２年間全く貢献していませんでした](https://www.reddit.com/r/Bitcoin/comments/6uec40/jeff_garzik_has_been_removed_from_the_bitcoin/)。そんな彼の GitHub アカウントにリポジトリ書き込み権限を残しておくことは、プロジェクトにとってメリットがないばかりか、セキュリティ上のリスクとなります。これはWladimir が投稿で言及した最小特権の原則に反します。

Bitcoin Core はテクノクラシーや象牙の塔のように参加ハードルが高いと感じる人もいるかもしれません。でも実際にコントリビューターと話せば、それは誤解だとわかるはずです。コミット権を持つのは[数十人](https://bitcointalk.org/index.php?topic=1774750.0)程度ですが、参加する開発者は数百人にのぼります。私もいくつか小さな貢献をしました。自分ではそうは思っていませんが、私はまぎれもなく「コア開発者」なのです。コントリビューターになりたいと思うなら、誰もあなたを止めたりしません。

「2011年、ポインターの意味すら知らなかった高校生の私が送ったひどいパッチを [@bitcoincoreorg](https://twitter.com/bitcoincoreorg) の開発者コミュニティ（特に Greb Maxwell や [@pwuille](https://twitter.com/pwuille) ）がマージできるものにすべく色々教えてくれました。学びの場としては最高の環境です。」[Matt Corallo](https://twitter.com/TheBlueMatt/status/1064292104346771458)（2018年11月18日）

「2016年に [@TheBlueMatt](https://twitter.com/TheBlueMatt) は [@ChaincodeLabs](https://twitter.com/ChaincodeLabs) でのトレーニングプログラムを企画しました。私はビットコインについて手に入るものは全て読んでいましたが、プルリクエストを送る勇気はありませんでした。そんな私に Matt、 Alex 、 Suhas は貴重な時間を割いてビットコインについて、ビットコインへの貢献方法について教えてくれました。」[John Newbery](https://twitter.com/jfnewbery/status/1064301049534664707)（2018年11月18日）

「 [@bitcoincoreorg](https://twitter.com/bitcoincoreorg) にマイナーなコミットをし、私が送ったプルリクエストについて [@MarcoFalke](https://twitter.com/MarcoFalke)、[@pwuille](https://twitter.com/pwuille)、[@orionwl](https://twitter.com/orionwl)、[@LukeDashjr](https://twitter.com/LukeDashjr) 、[@jfnewbery](https://twitter.com/jfnewbery) らと畏れ多くも議論しました。みんな親切で心温かい人たちです！」[Jeff Rade](https://twitter.com/jeffrade/status/1064593787756965893)（2018年11月19日）

多くの人が理解に苦しむものに、ビットコイン開発のフォーカルポイントは単に Bitcoin Core の GitHub アカウントを基盤とする開発体制**ではない**という事実があります。Bitcoin Core はある程度体系立っています（サブプロジェクトでは、調整プロセスは中央集権的なコミュニケーション手段に頼っています）。しかし、こうしたメンバーが Core プロジェクトを意のままに操ることはできません。そんなことは GitHub リポジトリで特別な権限を付与された人でも不可能です。メンテナーが結託してクーデターを起こして GitHub リポジトリを乗っ取り、対立する開発者を検閲したり、「 Bitcoin Core 」というブランド名を使い続けることは技術的には可能です。ただ、そんなことをすれば、 Bitcoin Core は開発のフォーカルポイントではなくなるでしょう。メンテナーの行動に抗議する開発者たちはコードをフォークし、Bitcoin Core のメンテナーが管理者権限を持たない別のリポジトリで開発を続けるでしょう。

「クーデーター」まで行かなくても、物議をかもすような変更が Core に加えられた場合、一部の開発者がコードをフォークして変更前の状態に戻したソフトウェアを配布することは十分考えられます。Amaury Sechet が Bitcoin Core をフォークしてSegWit（セグリゲイテッド・ウィットネス）機能を削除し、Bitcoin ABC を作った時がまさにそうでした。あるいは、一部の人々が望む変更を Core が拒否した場合も、開発者は Core のコードをフォークして変更を加えることができます。これは以下を含め、実際に何度も起きました。



* [Mike Hearn](https://medium.com/@octskyward) が Core のコードをフォークして Bitcoin XT を作成
* [Andrew Stone](https://g-andrew-stone.medium.com/) が Core のコードをフォークして Bitcoin Unlimited を作成
* [Jeff Garzik](https://medium.com/@jgarzik) が Core のコードをフォークして BTC1 を作成

コードをフォークするのは簡単ですが、ビットコイン開発のフォーカルポイントを移行するのは簡単ではありません。新しいプロジェクトに時間を費やす方が賢明だと Core コントリビューターたちを説得しなければなりません。

「ビットコインに関して、私は誰にも、どの開発チームにも忠誠を誓いません。私はただ、自らの金融主権を最も確実に守ることができると判断したコードを実行するだけです。」[Jameson Lopp](https://twitter.com/lopp/status/843210083588816896?s=20)（2017年3月18日）

もう一つよくある誤解に、ユーザーは Bitcoin Core の変更を黙って受け入れるしかないというものがあります。これはユーザーが自分に与えられた選択肢を理解した上で合意形成プロセスに参加しないなら、自らの権限の一部を開発者に移譲するも同然という自己強化型の思い込みなのかもしれません。しかし、2017年の UASF（ユーザー・アクティヴェイテッド・ソフトフォーク）運動はユーザーの力を見せつけました。[shaolinfry](https://medium.com/@shaolinfry) という仮名を名乗る匿名のビットコイン開発者が、8月1日前後に予測される特定のブロック高において、マイナーに SegWit 機能の有効化を強制する [BIP148](https://github.com/bitcoin/bips/blob/master/bip-0148.mediawiki) を提案しました。しかし、BIP148 は激しい物議を呼ぶ提案であったため、Bitcoin Core に採用されることはないと悟ったshaolinfry は、Core のコードをフォークして「 [Bitcoin UASF](https://github.com/UASF/bitcoin) 」ソフトウェアを配布しました。Bitcoin UASF のダウンロード数は[無視できないレベルにまで伸び](https://www.buybitcoinworldwide.com/uasf/)、このユーザーの支持が BIP148 の期限前にフォークのフォークを提案する[ BIP91](https://github.com/bitcoin/bips/blob/master/bip-0091.mediawiki) の採用をマイナーに促す[プレッシャー](https://hackernoon.com/bip-148-uasf-first-year-anniversary-a-new-system-of-governance-223907ec298b)として機能しました。

私が考える最高の Bitcoin Core コントリビューターとは、[オーナーシップを極限まで](https://www.youtube.com/watch?v=ljqra3BcqWM)発揮する人です。[John Newbery](https://medium.com/@jfnewbery) がまさにこれに該当します。CVE-2018-17144と呼ばれるコンセンサスバグを含んだコードは彼が書いたわけではありませんが、そのマージをレビューによって防げなかったこと、そしてテストケースを書いていながら見つけられなかったことに対して、今でも責任を感じています。

「CVE-2018-17144 バグの責任は私にある。」[John Newbery](http://twitter.com/jfnewbery/status/1044016889117192194)（2018年9月24日）

私たちは皆、サトシなのです。

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/DjYbsq3FXfM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>


### Bitcoin Core に貢献するには

Core コントリビューターとなるのは、気が遠くなるほど大変だと感じるかもしれませんが、やる気のある開発者を支援するリソースは豊富にあります。[ここに](https://bitcoincore.org/en/faq/contributing-code/)ガイドラインがありますが、[Jimmy Song](https://jimmysong.medium.com/) の「[Gentle Introduction to Bitcoin Core Development](https://bitcointechtalk.com/a-gentle-introduction-to-bitcoin-core-development-fdc95eaee6b8) 」から始める方が良いかもしれません。

Core 開発者 [Eric Lombrozo](https://medium.com/@elombrozo) も Core リポジトリ内の変更プロセスについて解説記事「 [The Bitcoin Core Merge Process](https://medium.com/@elombrozo/the-bitcoin-core-merge-process-74687a09d81d) 」を執筆しています。

[Alex B](https://medium.com/@bergealex4). は、[ビットコイン開発の背後にある哲学](https://medium.com/@bergealex4/the-tao-of-bitcoin-development-ff093c6155cd)について素晴らしい記事を書いています。真剣にコントリビューターになりたいと考える人は、これを読むことで大いに時間を節約できるでしょう。

慣れないうちは、[Bitcoin Core プルリクエスト・レビュークラブ](https://github.com/bitcoin-core-review-club/website)に参加して、コードレビューの流れを確認するのも良いでしょう。

具体例を挙げましょう。本記事執筆中に、 GitHub のコミット履歴の整合性を監査するため、自分のコンピュータで verify-commits.py スクリプトを実行したところ、問題に遭遇しました。開発者が今後同じ問題に煩わされることのないように、私は[ドキュメント改善のプルリクエストを送りました](https://github.com/bitcoin/bitcoin/pull/14809)。プルリクエスト履歴を見ればわかるように、４人の開発者が私のプルリクエストの改善法を提案をしてくれました。提案は Wiki マークアップの使い分けから Bash コマンドの簡略化、 verify-commits.py スクリプトで利用できる新しいパラメーターまで多岐にわたっていました。どの提案も理に叶っていたので、全てコードに取り入れて、自分のプルリクエストとして修正バージョンをプッシュしました。レビュークラブに参加していた開発者たちは、このプルリクエストを受け入れて、メンテナーの [Macro Falke](https://github.com/MarcoFalke) が0.18リリースに含めるためのタグ付けをしました。数日経過後も開発者からの異議申し立てがなかったため、このコードはメンテナー Samuel Dobson によって Core にマージされました。


### 結局、誰がビットコインを支配しているのか？

システムとしてのビットコインを完全に理解するのは事実上不可能だと私は[以前から言い続けています](https://www.coindesk.com/markets/2017/03/11/nobody-understands-bitcoin-and-thats-ok/)。プロトコルであるビットコインを定義（支配）することは、言語を定義するようなものです。言語は自然発生するもので、言葉の意味に関する合意は辞書に基づくのではなく、有機的に形成されます。辞書は言語を定義するのではなく、言語という事象を記述します。同様に、ビットコインの実装はコードを介してビットコインという言語を記述します。辞書に書かれた言葉の定義についての同意を強制されることがないように、特定のビットコインの実装コードを実行するよう強制されることもありません。

言語は民主主義に基づいて管理運営されてはいません。ビットコインも同じです。マイナー、ノード、開発者、ユーザーの「投票」に基づく管理運営法について耳にしたことがあるかもしれませんが、ビットコインには該当しません。多数派が望む変更を反対する少数派に強制同意、強制採用させる仕組みはビットコインにはありません。ビットコインは支配者のいない無政府主義です。支配者（ruler: ルーラー）はいませんが、規則（rule: ルール）はあります。規則はネットワーク参加者が各々定義、施行します。

ビットコインプロトコルの変更は通常[ビットコイン改善提案プロセス](https://github.com/bitcoin/bips/blob/master/README.mediawiki)（BIP）を経て反映されますが、BIP は単に推奨されるベストプラクティスという位置付けで、遵守を強制されることはありません。BIP はピアレビューと合意形成プロセスを通して実施可能な変更へと導く方法にすぎないのです。

これは説明するのも理解するのも難しいですが、これこそがビットコインの反脆弱性にとって非常に重要な側面です。もし管理中枢があったら、それはビットコインの成功に怯える個人や組織に悪用される単一障害点になり得ます。最終的には、ノード運営者が各々、他のネットワーク参加者が合意規則に違反していないことを確認することで、自らを管理しているのです。この[セキュリティモデル](https://www.coindesk.com/markets/2016/11/13/bitcoins-security-model-a-deep-dive/)が、ビットコインのボトムアップガバナンスの基礎です。

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/_IMzSCSeM68" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></center>

ビットコインをコントロールする者はいません。

ビットコイン開発のフォーカルポイントをコントロールする者もいないのです。


### 著作権等について
[利用規約 A](https://lostinbitcoin.jp/copyright/#uaa)
