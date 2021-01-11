最初のヘッダー | 2番目のヘッダー
--- | ---
コンテンツセル | コンテンツセル
コンテンツセル | コンテンツセル

![シタデル](https://vignette.wikia.nocookie.net/masseffect/images/d/d7/MassEffect2Citadel.jpg/revision/latest?cb=20100721191415)

左揃え | センターアライン | 右揃え
:-- | :-: | --:
列3は | いくつかの言葉のテキスト | **1600ドル**
列2は | 中央揃え | $ 12
ゼブラストライプ | きちんとしている | ~~ $ 1 ~~

Dillingerは、クラウド対応、モバイル対応、オフラインストレージ、AngularJSを利用したHTML5Markdownエディターです。

- 左側にMarkdownを入力します
- 右のHTMLを参照してください
- マジック

# true

- HTMLファイルをインポートして、魔法のようにMarkdownに変換されるのを見てください-SDFGHJKL：LKJHGFDFGHJKCMNHV
- 画像をドラッグアンドドロップします（Dropboxアカウントがリンクされている必要があります）

あなたもすることができます：

- GitHub、Dropbox、Googleドライブ、OneDriveからファイルをインポートして保存します
- マークダウンファイルとHTMLファイルをDillingerにドラッグアンドドロップします
- ドキュメントをMarkdown、HTML、PDFとしてエクスポートする

マークダウンは、人々が電子メールで自然に使用するフォーマット規則に基づく軽量マークアップ言語です。 [JohnGruber]が[Markdownサイト] [df1]に書いているように

> Markdownのフォーマット構文の最も重要な設計目標は、可能な限り読みやすくすることです。マークダウン形式のドキュメントは、タグやフォーマット手順でマークアップされているように見えることなく、プレーンテキストとしてそのまま公開できる必要があるという考え方です。

ここに表示されるこのテキストは、*実際に*はMarkdownで書かれています。 Markdownの構文の感触をつかむには、左側のウィンドウにテキストを入力し、右側の結果を確認します。

### false

Dillingerは、適切に機能するために多くのオープンソースプロジェクトを使用しています。

- [AngularJS] -Webアプリ用に拡張されたHTML！
- [エースエディター]-素晴らしいウェブベースのテキストエディター
- [markdown-it]-マークダウンパーサーは正しく実行されました。すばやく簡単に拡張できます。
- [TwitterBootstrap]-最新のWebアプリに最適なUIボイラープレート
- [node.js]-バックエンドのイベントI / O
- [Express]-高速node.jsネットワークアプリフレームワーク[@tjholowaychuk]
- [Gulp]-ストリーミングビルドシステム
- [ブレイクダンス-HTML](https://breakdance.github.io/breakdance/)からMarkdownへのコンバーター
- [jQuery]-当たり前

そしてもちろん、Dillinger自体はGitHubに[パブリックリポジトリ] [dill]を備えたオープンソースです。

### インストール

![イロス](https://lh3.googleusercontent.com/proxy/DDV8a7sLIWurhJtW8Ego9bq-JlwpfFFoR0tkLJQKKYXEXoWHB6ZUP5jGKD2VcYt3z1QVsgcn6L3GoU1ns8m9fvi3U51GzddA70ZUMHgzHvjl4-i7YOJY9cShBPrfjUhMQhxaJ97WFBp612XmjMXVGypfGkiBarN4PWxhiHkiYYNW7HGbtTpOcyt9GQ4Q23C2noxLTWFXZMcQZhRpQA_qzu2n6_H6CPViBnhSHpEl4JZAPaGCSJqgZg)

Dillingerを実行するには、 [Node.js](https://nodejs.org/) v4 +が必要です。

依存関係とdevDependenciesをインストールし、サーバーを起動します。

```sh
$ cd dillinger
$ npm install -d
$ node app
```

実稼働環境の場合...

```sh
$ npm install --production
$ NODE_ENV=production node app
```

### プラグイン

Dillingerは現在、次のプラグインで拡張されています。独自のアプリケーションでそれらを使用する方法の説明は、以下にリンクされています。

プラグイン | README
--- | ---
ドロップボックス | [plugins / dropbox / README.md] [PlDb]
GitHub | [plugins / github / README.md] [PlGh]
グーグルドライブ | [プラグイン/googledrive/README.md][PlGd]
OneDrive | [プラグイン/onedrive/README.md][PlOd]
中 | [プラグイン/メディア/README.md][PlMe]
グーグルアナリティクス | [プラグイン/googleanalytics/README.md][PlGa]

### 開発

貢献したいですか？すごい！

Dillingerは、高速開発のためにGulp + Webpackを使用しています。ファイルに変更を加えて、すぐに更新を確認してください。

お気に入りのターミナルを開き、これらのコマンドを実行します。

最初のタブ：

```sh
$ node app
```

2番目のタブ：

```sh
$ gulp watch
```

（オプション）3番目：

```sh
$ karma test
```

#### ソースの構築

製品リリースの場合：

```sh
$ gulp build --prod
```

配布用のビルド済みzipアーカイブの生成：

```sh
$ gulp build dist --prod
```

### Docker

Dillingerは、Dockerコンテナにインストールしてデプロイするのが非常に簡単です。

デフォルトでは、Dockerはポート8080を公開するため、必要に応じてDockerfile内でこれを変更します。準備ができたら、Dockerfileを使用してイメージをビルドします。

```sh
cd dillinger
docker build -t joemccann/dillinger:${package.json.version} .
```

これにより、ディリンジャーイメージが作成され、必要な依存関係が取得されます。 `${package.json.version}`を実際のバージョンのDillingerと交換してください。

完了したら、Dockerイメージを実行し、ホスト上の任意のポートにポートをマップします。この例では、ホストのポート8000をDockerのポート8080（またはDockerfileで公開されているポート）にマップするだけです。

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/dillinger:${package.json.version}
```

好みのブラウザでサーバーアドレスに移動して、展開を確認します。

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud

[KUBERNETES.mdを](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)参照してください

### Todos
