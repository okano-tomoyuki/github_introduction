# Preparing the usage environment for Git and GitHub

This document is draft!
Sorry, coming soon...

## 前提条件
- Windows(10以降)を利用していること
- 今までにSSHのキーペアを生成したことがないこと(SSHについては用語解説の項を参照)

## 用語解説
|名称|意味|
|--|--|
|Git Bash|Gitを利用するためのツール|
|Source Tree|GitをGUIから操作するためのツール(事前にGit Bashのインストールが必要)|
|SSH|通信の暗号化方式の一つ。秘密鍵と呼ばれるファイルをクライアントPCに、<br>公開鍵と呼ばれるファイルをGitHub上に保存することで機能する。|

## 1. Gitの利用環境準備
所要時間　30分

- Git Bashのインストール
- SSH秘密鍵、公開鍵のペアを作成
- Source Treeのインストール
- Source Treeで利用できるようにssh秘密鍵を変換

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

### 1.2 SSH秘密鍵、公開鍵のペアを作成
Git Bashを起動します。

下記コマンドを実行し秘密鍵、公開鍵のペアを作成します。

```
ssh-keygen -t rsa -b 4096 -C "自分のメールアドレス"
```

デフォルトであれば、「C:\Users\mesxxxxx」直下に.sshというフォルダが作成されています。(xxxxxはご自身の個人番号です。)
このフォルダの中にid_rsaとid_rsa.pubという2種類のファイルがありますが、id_rsaが秘密鍵ファイル、id_rsa.pubが公開鍵ファイルです。

### 1.3 Source Tree

下記リンクからインストーラーをダウンロードします。

https://www.atlassian.com/ja/software/sourcetree

Windows向けを選択

![step 1.2.1](/img/1.2/1.png)


## 2. GitHubの利用環境準備

- GitHubアカウントの作成
- GitHubアカウントにssh公開鍵の登録
- 
