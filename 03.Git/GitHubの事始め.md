パッケージのインストール
======================================

1. 前提
--------------------------------------
 - GitHubにリポジトリを作っておく
 - gitをインストールしておく

2. ローカルでの作業
--------------------------------------
gitにリモートリポジトリの場所を登録

	git remote add origin https://github.com/ryot0/memo.git

commitメッセージに含める名前とメールアドレス

	git config --global user.name "xx yy"
	git config --global user.email "xx@example.com"

認証する際のパスワードをOSのキーチェインに登録して管理する

	git config --global credential.helper osxkeychain

現在のブランチのみをpushする設定

	git config --global push.default simple

作業用ディレクトリをつくって初期化

	mkdir test
	git init

...なんやなんかややってindexに追加

	git add -A .

コミット

	git commit

GitHubにpush。-uをつけておくと、次回以降は、originを指定する必要がなく、git pushでOK

	git push -u origin master
