---
layout: "../../layouts/BlogPost.astro"
title: 'CSSでサイトを装飾する'
required_time: '10分'
id: 5
---

CSS を使うことで、文字の大きさを換えたり、背景の色を変えたりできます。

<br>

# # CSS でスタイルを設定する

`<head>` タグ内に `<style>` タグを追加して、スタイルの設定をします。



~~~astro
---
---
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>Astro</title>
		<style>
			h1 {background-color: gray;}
			p {color: olive; font-size: 20px;}
		</style>
	</head>
	<body>
		<h1>n1sym Blog</h1>
		<p>ここは n1sym の個人サイトです。</p>
	</body>
</html>
~~~

`<h1>` と `<p>` タグに対して、色や大きさの設定をしています。

プレビュー画面に反映されないときは、`<body>` タグ内の文章を書き換えれば反映されると思います。（もしくはプレビュー画面の更新ボタンをクリック）

色の一覧は以下で確認できます。

- https://developer.mozilla.org/ja/docs/Web/CSS/color_value

<br>

# # 個別にスタイルを当てる

上記では、タグそのものに対してスタイルを当てましたが、タグに `id` や `class` を割り振って、個別にスタイルを当てることもできます。

~~~astro
---
---
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>Astro</title>
		<style>
			h1 {background-color: gray;}
			p {color: olive; font-size: 20px;}
			#color-blue {color: blue;}
			.color-green {color: green;}
		</style>
	</head>
	<body>
		<h1>n1sym Blog</h1>
		<p>ここは n1sym の個人サイトです。</p>
		<p id="color-blue">2つ目の文章です。</p>
		<p class="color-green">3つ目の文章です。</p>
	</body>
</html>
~~~

`id="color-blue"` に対しては `#color-blue { ... }` 、`class="color-green"` に対しては `.color-green { ... }` という風にスタイルを当てます。

id の場合は頭に `#` を、class の場合は `.` を付けています。

同じ id はページ内で1回しか使えないので、複数タグに当てたいスタイルは class で書く必要があります。

CSSタグについて詳しく知りたい方は、以下の記事がおすすめです。

- https://saruwakakun.com/html-css/basic/css

<br>

# # 文字を中央寄せにする

`<style>` タグの中に `body {text-align: center;}` を追加することで、文字を中央寄せにすることができます。

<br>

# # 公開しているページに変更を反映させる

良い感じに CSS を設定することができたら、Commit ボタンで公開ページにも反映させてみましょう。