---
layout: "../../layouts/BlogPost.astro"
title: 'ブログ記事を作る'
required_time: '15分'
id: 8
---

サイトにブログ記事を投稿できるようにしてみましょう。

<br>

# # 必要なファイルを作成する

![](/image/post-8/dir.png)

上記の画像が完成系です。必要な作業は以下の通りです。

- `src` フォルダ内に、`layouts` フォルダを作成する
- `layouts` フォルダ内に `BlogPost.astro` ファイルを作成する
- `pages` フォルダ内に、`posts` フォルダを作成する
- `posts` フォルダ内に `2022-11-13.md` ファイルを作成する
  - ファイル名は任意で大丈夫です（拡張子は `.md` としてください）
- `pages` フォルダ内に、`blog.astro` ファイルを作成する

フォルダは以下のマークをクリックすることで作成できます。

![](/image/post-8/pages.png)

この時点では、作成したファイルの内容は空のままで問題ありません。

<br>

# # ブログ記事を書く

`2022-11-13.md` ファイルに内容を書き込みます。

~~~md
---
layout: "../../layouts/BlogPost.astro"
title: "はじめての記事"
date: "2022-11-13"
---

# はじめに

はじめてのブログです。

https://do-it-yourself.vercel.app/

# 画像の表示

![画像の説明](/yourself.png)
~~~

ブログ記事はマークダウン(`.md`) 記法で書きます。マークダウンは、文書を記述するための言語のひとつです。記法はとてもシンプルなので、各々調べてみてください。

`.md` ファイルだとページの見た目を設定できないので、`layout:` でページのレイアウトを設定するファイルを参照しています。 

<br>

# # レイアウトの設定

先ほど作った `BlogPost.astro` ファイルを編集します。以下のコードをコピペしてください。

~~~astro
---
const { content: { title, date } } = Astro.props;
---
<html lang="ja">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>{title}</title>
		<style >
		</style>
	</head>
	<body>
		<h1>{title}</h1>
		<p>{date}</p>
    <article>
      <slot />
    </article>
    <br>
    <a href="/blog">blog</a>
	</body>
</html>
~~~

サイトに表示されるブログ記事は、このファイルを元に描画されることになります。

`const { content: { title, date } } = Astro.props;` で `.md` ファイルに書いた `title` と `date` の情報を受け取っています。 

`<slot />` のところに、`.md` ファイルに書いた本文が埋め込まれます。

<br>

# # 記事一覧ページの作成

`blog.astro` ファイルを編集します。

~~~astro
---
const allPosts = await Astro.glob('../pages/posts/*.md')
---
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
		<meta name="viewport" content="width=device-width" />
		<meta name="generator" content={Astro.generator} />
		<title>Blog</title>
		<style>
		</style>
	</head>
	<body>
		<h1>Blog</h1>
    <ul>
      {allPosts.map((post) => <li><a href={post.url}>{post.frontmatter.title}</a></li>)}
    </ul>
    <a href="/">Home</a>
	</body>
</html>
~~~

`const allPosts = await Astro.glob('../pages/posts/*.md')` で、 `posts` フォルダにあるマークダウン形式のファイルを全て読み込んでいます。

それをループを回して、リスト形式で並べている... みたいなことをやっています。これは呪文のようなものなので、理解しなくても大丈夫なやつです。

こういう風に書くことで、`posts` フォルダにマークダウン形式のファイルを作成するだけで記事一覧ページに自動でその記事が追加されるようになります。

<br>

# # トップページにリンクを追加

トップページからブログ記事一覧ページに飛べるようにしておきます。

`index.astro` を編集します。リンクの数が増えてきたので、リスト形式で並べるようにしています。

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
		<style >
		</style>
	</head>
	<body>
		<h1>n1sym web</h1>
		<p>ここは n1sym の個人サイトです。</p>
		<ul>
			<li><a href="/about">about</a></li>
			<li><a href="/illust">illust</a></li>
			<li><a href="/blog">blog</a></li>
		</ul>
	</body>
</html>
~~~



これでプレビュー画面からブログ記事が見れるようになるはずです。

<br>

# # 公開しているページに変更を反映させる

記事が表示されていることが確認できたら、Commit ボタンをクリックして公開ページにも反映させてみましょう。