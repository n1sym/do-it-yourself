---
layout: "../../layouts/BlogPost.astro"
title: 'CSSでサイトを装飾する'
required_time: '10分'
id: 5
---

CSS を使うことで、Webページの文字の大きさを換えたり、背景の色を変えたりできます。

作成したサイトの見た目を調整してみましょう。

<br>

# # CSS でスタイルを設定する

`<head>` タグ内に `<style>` タグを追加して、スタイルの設定をします。

このスタイルは `index.astro` 、つまりトップページのみに有効な設定となります。

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
			h1 {background-color: gray;}
			p {color: olive; font-size: 20px;}
		</style>
	</head>
	<body>
		<h1>n1sym Page</h1>
		<p>ここは n1sym の個人サイトです。</p>
	</body>
</html>
~~~

`<h1>` タグの背景をグレーに、 `<p>` タグの文字色をオリーブ色にしています。

また、`<p>` タグの文字サイズも調整しています。このように `;` で区切ることで、複数のスタイルを当てることも可能です。

![](/image/post-5/style.png)

プレビュー画面に反映されないときは、`<body>` タグ内の文章を書き換えれば反映されると思います。（もしくはプレビュー画面の更新ボタンをクリック）

色の一覧は以下で確認できます。

- https://developer.mozilla.org/ja/docs/Web/CSS/color_value

<br>

# # 個別にスタイルを当てる

上記では、タグそのものに対してスタイルを当てましたが、タグに `id` や `class` を割り振って、個別にスタイルを当てることもできます。

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
			h1 {background-color: gray;}
			p {color: olive; font-size: 20px;}
			#color-blue {color: blue;}
			.color-green {color: green;}
		</style>
	</head>
	<body>
		<h1>n1sym Page</h1>
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

# # 公開しているページに変更を反映させる

良い感じに CSS を設定することができたら、Commit ボタンをクリックして公開ページにも反映させてみましょう。