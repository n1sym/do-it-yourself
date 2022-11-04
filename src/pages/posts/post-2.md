---
layout: "../../layouts/BlogPost.astro"
title: 'ソースコードを保存する'
required_time: '10分'
---


# # GitHub と連携する

ブラウザに開かれているソースコードを、GitHub に保存しましょう。

画面右上の Sign in というボタンをクリックすると、新しいウィンドウで Authorize の確認画面が表示されると思います。`Autorize stackblitz` という緑色のボタンをクリックして、GitHub と連携することを承認します。

連携が完了すると、ブラウザの右上に GitHub のプロフィールが表示されているはずです。

# # GitHub にソースコードを保存する

まずは画面左上の Fork ボタンを押します。

Fork が完了すると、画面左上に Connect repository というボタンが表示されるので、それをクリックします。

新しいウィンドウで Authorize の確認画面が表示されるので、`Autorize stackblitz` という緑色のボタンをクリックします。

すると、stackblitz の画面に以下のフィールドが出現します。 

![](/image/post-2/reponame.png)

New repository name: に、任意の名前を入力し、Create repo & push ボタンをクリックします。

Make this repository private には、**チェックをいれないでください。**

# # GitHub に保存したソースコードを確認する

Create repo & push が完了したら、画面の左上に作成したリポジトリの名前が表示されていると思います。

それをクリックすると、GitHub のリポジトリが開かれます。

![](/image/post-2/repo.png)

右上の About 欄に `stackblitz.com/edit/github-bvrdnh` というリンクが表示されていますが、これをクリックすると stackblitz の開発環境を開くことができます。