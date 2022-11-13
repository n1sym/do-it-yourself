---
layout: "../../layouts/BlogPost.astro"
title: 'デザインを調整する'
required_time: '15分'
id: 9
---

最後に、全体のデザインを調整してみましょう。

<br>

# # ページ全体にスタイルを当てる準備

ページ全体にスタイルを当てるために、新しいファイルを作成します。

- `src` フォルダ内に、`styles` フォルダを作成する
- `styles` フォルダ内に `global.css` ファイルを作成する

![](/image/post-9/styles.png)

そして、`global.css` に書いた設定を各ページに適用するため、

`import '../styles/global.css';` というコードを、

`index.astro`, `about.astro`, `blog.astro`, `illust.astro`, `BlogPost.astro` の

2行目（`---` と `---` の間）に追記します。

~~~astro
---
import '../styles/global.css';
---
~~~

<br>

# # デザインの調整

`global.css` を編集します。

~~~css
body {
	margin: auto;
	padding: 20px;
	max-width: 720px;
	text-align: left;
	background-color: #fff;
	word-wrap: break-word;
	overflow-wrap: break-word;
	line-height: 1.5;
	color: rgb(27, 26, 26);
}

img {
	max-width: 100%;
	height: auto;
}

blockquote {
	border-left: 3px solid #999;
	color: rgb(71, 71, 71);
	padding: 2px 0px 2px 20px;
	margin: 0px;
	font-style: italic;
}
~~~

それぞれの項目を見ていきます。

# ## body

まずは `<body>` タグに当てるスタイルについてです。`<body>` タグはざっくりとページの内容全てを表しているので、ここで設定したスタイルはページ全体に適用されます。

各要素の意味は以下のような感じです。

- `margin` : 外側の余白。`auto` を指定するとよしなに調整してくれる
- `padding` : 内側の余白
- `max-width` : 最大幅。このサイズ以上にはならない
- `text-align` : 要素の寄せ。今回は左寄せ(`left`) を指定
- `background-color` : 背景色
- `word-wrap`: 文字の折り返しタイミングの設定
- `overflow-wrap`: 文字の折り返しタイミングの設定
- `line-height`: 文字の高さ
- `color`: 文字の色

ブラウザ上でカラーコードにカーソルを合わせると、カラーパレットが表示されるのでそこで色を設定することもできます。

![](/image/post-9/color.png)

# ## img

`<img>` タグは画像に関するタグです。

~~~css
img {
	max-width: 100%;
	height: auto;
}
~~~

初期設定のままだと、大きい画像がそのまま表示されてしまいます。`body` のスタイルで設定した最大幅 (`max-width`) に合わせて自動でリサイズされるようになってほしいので、上記の設定を行っています。

# ## blockquote

`<blockquote>` は引用を表現するタグです。初期設定だとインデントされるだけなので、それっぽいデザインにしておきます。

![](/image/post-9/blockquote.png)

~~~css
blockquote {
	border-left: 3px solid #999;
	color: rgb(71, 71, 71);
	padding: 2px 0px 2px 20px;
	margin: 0px;
	font-style: italic;
}
~~~

<br>

# # 公開しているページに変更を反映させる

スタイルは無限にこだわることができるので、一旦ここまでにしておきます。

Commit ボタンをクリックして公開ページにも反映させてみましょう。