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
- Source Treeのインストール
- ssh秘密鍵、公開鍵のペアを作成
- Source Treeで利用できるようにssh秘密鍵を変換

### 1.1 Git Bashのインストール

下記リンクからインストーラーをダウンロードします。

https://git-scm.com/download/win

「Standalone Installer」の「64-bit Git for Windows Setup.」を選択し、ダウンロードします。
インストーラーを起動し、インストール作業を行います。
![step 1.1](/img/1.png)

![step 2](/img/2.png)
![step 3](/img/3.png)
![step 4](/img/4.png)
![step 5](/img/5.png)
![step 6](/img/6.png)
![step 7](/img/7.png)
![step 8](/img/8.png)


## 2. GitHubの利用環境準備

- GitHubアカウントの作成
- GitHubアカウントにssh公開鍵の登録
- 
