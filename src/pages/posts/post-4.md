---
layout: "../../layouts/BlogPost.astro"
title: 'トップページを作る'
required_time: '10分'
id: 4
---

サイトをカスタマイズしていきます。

<br>

# # stackblitz の開発環境を開く

stackblitz の開発環境を閉じてしまった方は、GitHub に作成したリポジトリから再び開くことができます。右上の About 欄にリンクが表示されていると思います。

![](/image/post-4/about.png)

<br>

# # トップページを編集する

ファイルツリーから `src` > `pages` > `index.astro` を選択してクリックします。

![](/image/post-1/filetree.png)

この `index.astro` というのが、トップページの画面を作っているファイルとなっています。

早速 `index.astro` を書き換えていきます。

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
	</head>
	<body>
		<h1>n1sym Blog</h1>
		<p>ここは n1sym の個人サイトです。</p>
	</body>
</html>
~~~

`<h1>`タグの下に、`<p>`タグを追加して、文章を入れてみました。上記のコードはあくまで例なので、何かお好きな文章を入れてみてください。

プレビュー画面にも変更が反映されていると思います。

<br>

# # 色々な HTML タグ

基本的な HTML タグを試しに使ってみましょう。

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
	</head>
	<body>
		<h1>n1sym Blog</h1>
		<p>ここは n1sym の個人サイトです。</p>

		<hr>

		<h2>見出し 2</h2>
		<h4>見出し 4</h4>
		<h6>見出し 6</h6>

		<p>ここで<br>改行します。</p>

		<ul>
			<li>ひとつめの項目</li>
			<li>ふたつめの項目</li>
			<li>みっつめの項目</li>
		</ul>

		<a href="https://twitter.com/n1sym">これはツイッターへのリンクです</a>
	</body>
</html>
~~~

HTMLタグについて詳しく知りたい方は、以下の記事がおすすめです。

- https://saruwakakun.com/html-css/basic/html

<br>

# # 公開しているページに変更を反映させる

ある程度トップページの形が整ったら、 公開しているページに変更を反映させてみましょう。

StackBlitz の左上に表示されている `Commit` という青いボタンを押します。

以下の画面が表示されると思うので、もう一度 `Commit` という青いボタンを押します。（Commit message: は任意のメッセージに書き換えても大丈夫です）

![](/image/post-4/commit.png)

以下の警告が出たら、Save anyway ... をクリックすれば大丈夫です。

![](/image/post-4/isok.png))

Commit が完了したら、1~2分くらいで公開しているページに変更が反映されます。