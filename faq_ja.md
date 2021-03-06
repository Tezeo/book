# よくある質問

## どのようにバグや要望を報告すればいいでしょうか？ ?

いつでも[support@exploratory.io](mailto:support@exploratory.io) からお問い合わせ下さい。

## Exploratoryの更新を知るのに一番いい方法は何でしょうか？

Twitterの[@KanAugust](https://twitter.com/KanAugust) をフォローするか、私たちのブログをサブスクライブしてください: http://blog.exploratory.io .

## Mac OS X はサポートされていますか ?

サポートしています! 公式的には、El Capitan と Yosemiteをサポートしていますが、Mavericksでも問題なく動くはずです.

## Windowsはサポートされていますか ?

まずWindows 10 と8 をサポートするために現在開発中です。正確な日程をお約束することはできませんが、おそらく、もうすぐにWindowsにも対応する予定です。その時が来たら正式に発表しますので、少しお待ち下さい。

## Linuxはサポートされていますか ?

Linuxでも同様に動くようにする予定です。

## どうして、私のOS Xのパスワードを尋ねるんですか？

もし、以前にRやGitがお客様のパソコンにインストールされていなかったら、お客様のMac OSの管理者権限のユーザーネームとパスワードを、尋ねられると思います。これは、RとGitのインストールが、システムの管理者権限を必要としているからです。Exploratoryは、そのときのお客様のパスワードの情報を知ることはありません。それは、完全にRとGitのインストールのためによるものであり、Exploratoryとは関係がありません。

## ネットワーク接続にトラブルがあります。どうすればいいですか？

Exploratoryは、ユーザーの認証を行ったり、もしあなたがまだインストールしていない場合は、GitやRのようなExploratoryに必要なソフトウェアをダウンロードしたり、Google AnalyticsやWebスクレイピングのようなリモートのデータにアクセスしたり、ノートを公開するためにインターネットに接続している必要があります。ただし、最初のセットアップさえ終わっていれば、オフラインでもExploratoryでデータを分析していくことはできます。

もし、インターネットに接続するために、プロキシサーバーを使っている場合は、デフォルトで、自動的にプロキシサーバーを見つけようとしたり、サーバーを通じて接続しようとします。これは、ほとんどの場合うまく作動しますが、特定のケースにおいてうまくいきません。そのときは、手動で、Mac OS Xでは~/.exploratory、Windowsでは、<your_user_home_folder>/.exploratoryのところに置かれているuserconf.json ファイルにあなたのプロキシサーバーの情報を加えることで解決することができます。例えば、下記のような形になります。

**Set a proxy server:**

```
{
   "user": "dummy1",
   "proxy": {
     "server": "<your_proxy_server>",
     "port": <port_number>,
     "user": "<username>",
     "password": "<password>"
   }
}
```

いったんプロキシサーバーの情報をセットすると、ファイルを保存してExploratoryを再起動してください。もしそれでもまだネットワークのトラブルに合う場合は、support@exploratory.ioまでご連絡ください。

## 私は、すでにR (rstats) 3.2をインストールしていますが、今すぐに3.3にアップグレードしたくありません。

R 3.2のためのExploratoryデスクトップアプリケーションを準備しています。ダウンロードページのダウンロードボタンのすぐ下にある'Are you R 3.2 users?'というリンクをクリックしてください。これで、R 3.2のExploratoryをダウンロードすることができるようになります。このバージョンは、あなたのRのバージョンをチェックし、Rのバージョンが3.2.0以降であれば、Rをインストールしません。

ただし、最新版のExploratoryでは、R3.3が必要となります。

## 私はすでにR (rstats) 3.3をインポートしています。Exploratoryでは、また別のRをインストールする予定ですか？

いいえ、違います。あなたのパソコンのRのバージョンをチェックしているだけです。Rのバージョンが3.3.0やそれより新しい場合である限り、Exploratoryは、Rを新しくインストールしないで、すでにインストールされているRを使います。

## 私はRをインストールしたことがありませんが？

ダウンロードページからダウンロードボタンを押してExploratoryをダウンロードしてください。初期のセットアップの一部としてRをインストールします。

## 私は、Mac OS XでHomebrewでRをインストールしていますが、大丈夫ですか？

残念なことに、今はまだ、HomebrewによってインストールされたRは、サポートしていません。Exploratoryは、あなたのデータ分析をもっと効率よくするために一連のRのパッケージが必要です。それらのパッケージをインストールする場合、Exploratoryは、CRANからインストールした.pkgとついた通常のインストーラーからインストールされているRを想定しています。もし、お客様がExploratoryを使いたい場合の解決策は、下記のコマンドによって、いったんRを削除しExploratoryを再起動してください。Exploratoryの方でCRAN標準のRを自動的に再インストールいたします。

```
> brew uninstall r
```

## Rの何のバージョンが必要ですか  ?

- ExploratoryのR (rstats) 3.2のバージョンでは、R 3.2.0かそれ以上。
- ExploratoryのR (rstats) 3.3バージョンでは、R 3.3.0かそれ以上。

## Gitの何のバージョンが必要ですか?

Git 2.0.0かそれ以上が必要です。Gitの古いバージョンを見つけない限り、Gitをインストールしません。 Exploratoryは、Gitは、/usr/bin か /usr/local/binの直下にあると想定しています。もし何らかの理由で、あなたのGitがどこか違うところにインストールされている場合は、ExploratoryがGitがないと判断して、インストールしはじめようとするかもしれません。その場合は、Gitが新しくインストールされるのを待たないで、support@exploratory.ioまで連絡してください。

## どんなRのパッケージをインストールしていて、それはなぜですか？

Exploratoryデスクトップアプリケーションでは、驚くべき数のRのパッケージを使っています。そのほとんどが、効率よく楽しくデータ分析をすることを可能にするHadleyverseに関連したものです。お客様は、最初のセットアップ画面で　'See a list of software and libraries to be installed.'をクリックすることでインストールされるRのパッケージを確認することができます。

## Rのパッケージはどこにインストールしていますか？

Exploratoryデスクトップアプリケーションの1.4.1かそれ以降である最新のバージョンでは、普通のRをインストールする場所とは違って、Exploratoryのレポジトリにインストールしています。これは、お客様の既にインストール済みのパッケージとコンフリクトを起こすのを防ぐためです。

## 私のお気に入りのRパッケージを加えることはできますか？

近いうちにサポートする予定です。もし、そのような要望がある場合は、ぜひsupport@exploratory.ioまで連絡してください。お客様の要望を元にどのようにサポートするのが最適かを理解したいと思っております。

## 私が扱ってるデータは機密扱いです。私のデータは、どこに保管されているのですか？

いったんあなたのデータがExploratoryにインポートされると、あなたのパソコンの~/.exploratoryの直下にあるExploratoryのレポジトリの中に保存されます。あなたのデータは、あなたのパソコンにあるままで、決してあなたのパソコンから外に出ることはありません。

## 私のユーザーネームを変更することはできますか？

今はまだ、ユーザーネームを変更することはできません。しかし、将来的には、変更することができるようになります。もし、どうしても変更されたい場合は、support@exploratory.ioに連絡してください。手動で、お客様のユーザーネームを変更させていただきます。
