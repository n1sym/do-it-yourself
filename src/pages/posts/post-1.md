---
layout: "../../layouts/BlogPost.astro"
title: '開発環境を立ち上げる'
required_time: '10分'
id: 1
---

何事も始めは「小さく作る」のがおすすめです。

まずは簡単なサイトを作って、公開してみるところから始めてみましょう。

<br>

# # 開発環境を立ち上げる

ここでは StackBlitz という、ブラウザ上で開発環境を構築できるサービスを利用します。

以下のURLを開くと、自動で開発環境がセットアップされます。

初期設定だと黒を基調としたダークテーマになっていると思いますが、画面左下の半月ボタンを押せば明るい背景にすることもできます。

https://astro.new/minimal?on=stackblitz

![](/image/post-1/astro.png)

画面は大きく3列に分けられています。

今回主に操作するのは、左列のファイルツリー、中央のエディタになります。（初期状態では `README.md` というファイルが開かれており、内容を編集できるようになっています）

右側には、現在のサイトのプレビューが表示されています。実はもう既に Webサイト作成に必要なファイルが一式揃えられており、現在は **Astro**  という文字が表示されるようになっています。

<br>

# # 表示されている文字を編集してみる

ファイルツリーから `src` > `pages` > `index.astro` を選択してクリックしてみましょう。

![](/image/post-1/filetree.png)

中央のエディタに、以下の内容が表示されると思います。

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
		<h1>Astro</h1>
	</body>
</html>
~~~

この内容は、右側のプレビューされている画面と対応しています。つまり、今のプレビュー画面は `index.astro` の内容を表示しているということになります。

`<h1>Astro</h1>` の Astro という文字を任意の文字に変更してみましょう。プレビュー画面に内容が反映されるはずです。（その他の htmlタグについては今は考えなくても大丈夫です）