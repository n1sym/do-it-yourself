---
layout: "../../layouts/BlogPost.astro"
title: 'ソースコードを保存する'
required_time: '5分'
id: 2
---

StackBlitz で開いているソースコードを、GitHub に保存してみましょう。

<br>


# # GitHub と連携する

![](/image/post-2/signin.png)

画面右上の Sign in というボタンをクリックすると、新しいウィンドウで Authorize の確認画面が表示されると思います。`Autorize stackblitz` という緑色のボタンをクリックして、GitHub と連携することを承認します。

連携が完了すると、画面の右上に GitHub のプロフィールが表示されているはずです。

<br>

# # GitHub にソースコードを保存する

まずは画面左上の Fork ボタンを押します。

Fork が完了すると、画面左上に Connect repository というボタンが表示されるので、それをクリックします。

新しいウィンドウで Authorize の確認画面が表示されるので、`Autorize stackblitz` という緑色のボタンをクリックします。

すると、stackblitz の画面に以下のフィールドが出現します。 

![](/image/post-2/reponame.png)

Make this repository private には、**チェックをいれないでください。**

New repository name: に、任意の名前を入力し、Create repo & push ボタンをクリックします。

repository （リポジトリ）は GitHub の用語で、ファイルやフォルダを記録する場所のことを指します。



<br>

# # GitHub に保存したソースコードを確認する

Create repo & push が完了したら、画面の左上に作成したリポジトリの名前が表示されていると思います。

![](/image/post-2/name.png)

それをクリックすると、GitHub のリポジトリが開かれます。

![](/image/post-2/repo.png)

右上の About 欄に `stackblitz.com/edit/github-bvrdnh` というリンクが表示されていますが、これをクリックすると stackblitz の開発環境を開くことができます。