# Preparing the usage environment for Git and GitHub

所要時間　30分

This document is draft!
Sorry, coming soon...

## 前提条件
- Windows(10以降)を利用していること
- SMSが受信可能でMFA用のアプリケーションのインストールが可能なスマートフォン等の端末を保持していること
- ~~今までにSSHのキーペアを生成したことがないこと~~ (注)SSHの場合社内DNSから名前解決できないためHTTPSを使用する

## 用語解説
|名称|意味|
|--|--|
|Git Bash|Gitを利用するためのツール|
|Source Tree|GitをGUIから操作するためのツール(事前にGit Bashのインストールが必要)|
|SSH|暗号化した通信手段の一つ(Secure Shell)。秘密鍵と呼ばれるファイルをクライアントPCに、<br>公開鍵と呼ばれるファイルをGitHub上に保存することで機能する。|
|MFA|多要素認証(Multi Factor Authentication)。アカウントの乗っ取りなどを防ぐために設定する必要がある。|

## 1. GitHubの利用環境準備

- GitHubアカウントの作成
- MFAの設定

## 2. Gitの利用環境準備

- Git Bashのインストール
- Source Treeのインストール
- Source Treeからの疎通確認

### 2.1 Git Bashのインストール

下記リンクからインストーラーをダウンロードします。

https://git-scm.com/download/win

「Standalone Installer」の「64-bit Git for Windows Setup.」を選択し、ダウンロードします。

![step 2.1.1](/img/2.1/1.png)

ダウンロードしたインストーラーを起動し、インストール作業を行います。

![step 2.1.2](/img/2.1/2.png)

下記画面が起動します。「Next」をクリックします。
以降インストールまですべてデフォルト設定のまま「Next」をクリックして進めてください。

![step 2.1.3](/img/2.1/3.png)

インストール実行後以下の画面が表示されます。
「View Release Notes」のチェックボックスを外し、「Finish」をクリックします。
(外さなくても問題はありません。リリースノートページのリンクが開くだけです)

![step 2.1.2](/img/2.1/4.png)

次にインストールしたGitに初期設定を行います。

### 2.2 Gitの初期設定
Git Bashを起動します。

Windows画面左下の検索ボックスに「Git Bash」と入力すると
選択画面が表示されるので、「開く」をクリックします。

![step 1.2.1](/img/1.2/1.png)

まず、gitを利用するユーザ名を入力します。ユーザ名は任意です。

```
git config --global user.name "[ユーザ名]"
```

次にメールアドレスを設定しましょう。

```
git config --global user.email "[会社のメールアドレス]"
```

次にプロキシサーバーの設定をしましょう。プロキシサーバー情報については岡野まで問い合わせください。
また、プロキシサーバーの設定情報は定期的に変更されるため**下記コマンドは定期的に実行する必要があります。**

```
git config --global http.https://github.com.proxy http://[プロキシサーバのユーザID]:[パスワード]@[サーバ名]:[ポート番号]
```

次にエンドポイント情報をHTTPS用のものに置き換えるように下記コマンドを実行します。
(社内プロキシ経由の場合、SSHが利用できない。)

```
git config --global url."https://github.com/".insteadOf git@github.com:
```

複数のリポジトリをまとめて管理するためのフォルダを作成し、移動します。

```
mkdir -p /c/source/meguri && cd /c/source/meguri
```

```
git clone git@github.com:okano-tomoyuki/test_private_repository.git
```

下記コマンドを実行し、リポジトリをcloneできているか確認します。

```
ls
```

確認ができたらcloneしてきたリポジトリを削除します。

```
rm -rf test_private_repository
```

### 2.3 Source Tree

下記リンクを参考に「環境設定」の項まで設定を行ってください。

https://yu-report.com/entry/sourcetree/
