---
title: GitHubでプルリクエストを送る方法
taxonomy:
    category:<!--- wikiの「1-2-2. カテゴリ & サブカテゴリの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - tutorial
    post_tag:<!--- wikiの「1-2-3. タグの一覧」から該当するものを選び、slugを入力（複数選択可） --->
        - beginner
---

## [用語集](https://lostinbitcoin.sakuraweb.com/glossary/glossary-index/)の翻訳・修正提案を例に、GitHubでプルリクエストを送る手順を解説
---

<button class="zap-button" data-npub="npub17d7ham6ucsm2yxuwa9k9th49d44lfa50uk2fq0v2p0jxs2npnyxsaxxt59" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button>

（[@akipponn](https://twitter.com/akipponn) さん、ガイド作成ありがとうございます。）

<!--- コンテンツの意図や要約文（省略可） --->
[用語集](https://lostinbitcoin.sakuraweb.com/glossary/glossary-index/)の用語の訳文の変更履歴の管理には、プログラムのソースコードのバージョン管理に利用されることの多いGitHubを利用しています。本記事では、GitHub上で翻訳・修正提案を作成し、送信する方法を説明します。

## 用語の説明
はじめに、Git/GitHubの用語を説明します。
- リポジトリ: プロジェクトのファイルや変更履歴をためておくデータベースのようなもの、または場所を表します。
- フォーク: 既存のリポジトリを完全にコピーして作られたリポジトリで、自由に変更を加えることができます
- ブランチ: 他の作業に影響を与えずに、新たな変更を加えられる作業スペースです。
- コミット: ファイルに対する変更を記録することです。
- プルリクエスト: 自分が行った変更を元のプロジェクトに取り込んでもらうリクエストです。

## 初回作業の流れ
1. <b>GitHubアカウントの作成:</b> [GitHub](https://github.com/)のアカウントを持っていない場合は、GitHubでアカウントを作成します。
1. <b>プロジェクトのリポジトリを開く:</b> GitHub上にある[ロストイン・ビットコインのリポジトリ](https://github.com/lostinbitcoin/categories/)を開きます。
1. <b>フォークの作成:</b> リポジトリのページの右上にある「Fork」ボタンをクリックすると、自分のアカウントの下にロストイン・ビットコインのリポジトリのフォークが作成されます。
![](/_images/PR_how_to-fork.png)
1. <b>リポジトリの選択:</b>自分のリポジトリのリスト（https://github.com/<GitHubのユーザー名>?tab=repositories）から、前のステップでフォークしたリポジトリ（https://github.com/<GitHubのユーザー名>/categories）を選びます。
1. <b>ブランチの作成:</b> ブランチのドロップダウンメニューをクリックします。新しいブランチ名（例えば、「translate_XXX」など）を英数記号で入力すると、「Create branch: [ブランチ名]」と表示され、クリックするとブランチが作成されます。![](/_images/PR_how_to-make_branch.png)
1. <b>ファイルの編集:</b> 作成したブランチで翻訳したいファイルを選択し、「Edit」ボタンをクリックし、ファイルの内容を編集します。どのブランチで作業しているのかは、画面左のメニューなどで確認できるほか、ファイルのURLでも確認できます。
![](/_images/PR_how_to-edit.png)
1. <b>コミット:</b> 編集が終わったら、「Commit changes」ボタンをクリックして、メッセージを記入し、変更をコミットします。この段階では、変更は自分のリポジトリのみに保存されます。
1. <b>プルリクエストの作成:</b> ロストイン・ビットコインのリポジトリに変更を提案する「プルリクエスト」を送ります。フォークしたリポジトリの「Pull requests」タブで、「New pull request」ボタンをクリックします。
![](/_images/PR_how_to-PR_01.png)
1. 変更を加えたブランチを選択し、内容を確認し、「Create pull request」ボタンをクリックします。
![](/_images/PR_how_to-PR_02.png)
1. <b>プルリクエストの詳細を記入・送信:</b> プルリクエストのタイトルと詳細を記入し、「Create pull request」ボタンをクリックすると、プルリクエストが送信されます。
![](/_images/PR_how_to-PR_03.png)

## 初回以降の作業の流れ
1. <b>リポジトリの同期:</b> 自分のアカウントの下にフォークしたリポジトリで、「Sync fork」をクリックして、ロストイン・ビットコインのリポジトリと同期します。
![](/_images/PR_how_to-sync.png)
1. 初回作業の「ブランチの作成」から「プルリクエストの詳細を記入・送信」までを行います。
