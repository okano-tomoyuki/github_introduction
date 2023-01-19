# Preparing the usage environment for Git and GitHub

This document is draft!
Sorry, coming soon...

## 前提条件
- Windows(10以降)を利用していること
- ~~今までにSSHのキーペアを生成したことがないこと~~ (注)SSHの場合MES-SのDNSから名前解決できないためHTTPSを使用する

## 用語解説
|名称|意味|
|--|--|
|Git Bash|Gitを利用するためのツール|
|Source Tree|GitをGUIから操作するためのツール(事前にGit Bashのインストールが必要)|
|~~SSH~~|~~通信の暗号化方式の一つ。秘密鍵と呼ばれるファイルをクライアントPCに、<br>公開鍵と呼ばれるファイルをGitHub上に保存することで機能する。~~|

## 1. Gitの利用環境準備
所要時間　30分

- Git Bashのインストール
- ~~Gitの初期設定、SSH秘密鍵/公開鍵のペアを作成~~ (注)HTTPSを使用する。
- Source Treeのインストール
- ~~Source Treeで利用できるようにssh秘密鍵を変換~~ (注)HTTPSを使用する。
- Source Treeからの疎通確認

### 1.1 Git Bashのインストール

下記リンクからインストーラーをダウンロードします。

https://git-scm.com/download/win

「Standalone Installer」の「64-bit Git for Windows Setup.」を選択し、ダウンロードします。
インストーラーを起動し、インストール作業を行います。
(後からでも変更可能なため、今回はすべてデフォルトの設定でインストールしていただいて結構です。)

![step 1.1.1](/img/1.1/1.png)

「Next」をクリックします。

![step 1.1.2](/img/1.1/2.png)

「Next」をクリックします。

![step 1.1.3](/img/1.1/3.png)

「Next」をクリックします。

![step 1.1.4](/img/1.1/4.png)

「Next」をクリックします。

![step 1.1.5](/img/1.1/5.png)

「Next」をクリックします。

![step 1.1.6](/img/1.1/6.png)

「Next」をクリックします。

![step 1.1.7](/img/1.1/7.png)

「Next」をクリックします。

![step 1.1.8](/img/1.1/8.png)

「Next」をクリックします。

![step 1.1.9](/img/1.1/9.png)

「Next」をクリックします。

![step 1.1.10](/img/1.1/10.png)

「Next」をクリックします。

![step 1.1.11](/img/1.1/11.png)

「Next」をクリックします。

![step 1.1.12](/img/1.1/12.png)

「Next」をクリックします。

![step 1.1.13](/img/1.1/13.png)

「Next」をクリックします。

![step 1.1.14](/img/1.1/14.png)

「Next」をクリックします。

![step 1.1.15](/img/1.1/15.png)

「Next」をクリックします。

![step 1.1.16](/img/1.1/16.png)

「Install」をクリックします。

![step 1.1.17](/img/1.1/17.png)

インストール実行後以下の画面が表示されます。
「View Release Notes」のチェックボックスを外し、「Finish」をクリックします。
(外さなくても問題はありません。リリースノートページのリンクが開くだけです)

![step 1.1.18](/img/1.1/18.png)


### 1.2 Gitの初期設定、~~SSH秘密鍵/公開鍵のペアを作成~~
Git Bashを起動します。

Windows画面左下の検索ボックスに「Git Bash」と入力すると
選択画面が表示されるので、「開く」をクリックします。

![step 1.2.1](/img/1.2/1.png)

```
git config --global user.name "[ユーザ名]"
```

```
git config --global user.email "[会社のメールアドレス]"
```

```
git config --global http.https://github.com.proxy http://[プロキシサーバのユーザID]:[パスワード]@[サーバ名]:[ポート番号]
```

```
git config --global url."https://".insteadOf git@
```

### 1.3 Source Tree

下記リンクからインストーラーをダウンロードします。

https://www.atlassian.com/ja/software/sourcetree

Windows向けを選択

![step 1.3.1](/img/1.3/1.png)


## 2. GitHubの利用環境準備

- GitHubアカウントの作成
- GitHubアカウントにssh公開鍵の登録
- 
