---
layout: "../../layouts/BlogPost.astro"
title: 'サイトを公開する'
required_time: '10分'
---

stackblitz で作ったサイトを公開してみましょう。

<br>

# # Vercel にログインする

サイトの公開は Vercel というサービスを利用します。

Vercel は GitHub アカウントを用いてログインをすることができます。以下のURLを開いて、

https://vercel.com/login


![](/image/post-3/login.png)

Continue with GitHub ボタンをクリックします。

Authorize の確認画面が出たら、Authorize Vercel という緑色のボタンをクリックしてください。

<br>

# # Vercel でサイトを公開する

ログインができたら、以下のURLを開いてください。

https://vercel.com/new

![](/image/post-3/import.png)

Continue with GitHub を選択します。

![](/image/post-3/search.png)

検索バーで作成したリポジトリの名前を入力し、Import ボタンをクリックします。

![](/image/post-3/config.png)

初期設定のままで問題ありませんので、Deploy ボタンをクリックします。

サイトの公開は数十秒で完了すると思います。

Congraturations! の画面に移動したら、Continue to Dashboard ボタンをクリックします。

![](/image/post-3/dashboard.png)

STATUS が Ready になっていたら、サイトが公開されています。DOMAINS 欄に表示されているURLを開いてみましょう。

stackblitz のプレビュー画面に表示されていたようなページが確認できると思います。

これにてひとまず、自分だけの個人サイトが作成できました。