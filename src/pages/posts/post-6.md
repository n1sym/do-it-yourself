---
layout: "../../layouts/BlogPost.astro"
title: '新しいページを作る'
required_time: '10分'
id: 6
---

トップページ以外にもページを作ってみましょう。

<br>

# # About ページの作成

自己紹介用のページを作ってみます。

ファイルツリーの `pages` フォルダにカーソルを合わせ、ファイル作成ボタンを押します。

![](/image/post-6/pages.png)

ファイルの名前は `about.astro` としてください。

![](/image/post-6/about.png)

ファイルの内容は、ひとまず以下のようにしておきます。

~~~astro
---
---
<html lang="ja">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>About</title>
		<style>
		</style>
	</head>
	<body>
		<h1>About</h1>
		<p>n1sym と申します。</p>
    <p><a href="https://twitter.com/n1sym">Twitter</a> をやっています。</p> 
    <a href="/">Home</a>
	</body>
</html>
~~~

`<a>` タグはリンクを表すものです。`href` でURLを指定することができます。

ちょっとややこしいのですが、`href="/"` の `/` は `index.astro` を指しています。つまりこれはトップページへのリンクになっています。

`index.astro` にもページ内リンクを配置します。

~~~astro
---
---
<html lang="ja">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>n1sym Page</title>
		<style>
		</style>
	</head>
	<body>
		<h1>n1sym</h1>
		<p>ここは n1sym の個人サイトです。</p>
		<a href="/about">about</a>
	</body>
</html>
~~~

プレビュー画面のリンクから、新しく作ったページに遷移してみましょう。

<br>

# # 公開しているページに変更を反映させる

新しいページを作成できたら、Commit ボタンをクリックして公開ページにも反映させてみましょう。