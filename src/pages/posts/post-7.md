---
layout: "../../layouts/BlogPost.astro"
title: '画像を表示する'
required_time: '5分'
id: 7
---

サイトに画像を載せてみましょう。

<br>

# # 画像をアップロードする

ファイルツリーの `public` フォルダに任意の画像をドラッグアンドドロップすることで、画像をアップロードします。

![](/image/post-7/public.png)

<br>

# # 画像を表示するためのページを作る

前回と同じように新しいページ `illust.astro` を作ります。

![](/image/post-7/illust.png)

~~~astro
---
---
<html lang="ja">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>画像置き場</title>
		<style>
		</style>
	</head>
	<body>
		<h1>画像置き場</h1>
		<img src="yourself.png" alt="do it yourself !!">
    <br>
    <a href="/">Home</a>
	</body>
</html>
~~~

`<img>` タグの `src` にはアップロードした画像のファイル名を、`alt` には画像の説明を入力します。


`index.astro` にページ内リンクを配置します。

~~~astro
---
---
<html lang="ja">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>Astro</title>
		<style>
		</style>
	</head>
	<body>
		<h1>n1sym</h1>
		<p>ここは n1sym の個人サイトです。</p>
		<a href="/about">about</a>
		<a href="/illust">illust</a>
	</body>
</html>
~~~

画像が表示されていることを確認してみましょう。

<br>

# # 公開しているページに変更を反映させる

画像が表示出来たら、Commit ボタンで公開ページにも反映させてみましょう。