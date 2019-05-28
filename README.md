Re Robust
===
このテーマは [Robust](https://github.com/dim0627/hugo_theme_robust) をベースに作成しました。  
基本的にデザインはそのままですが内部的に機能を強化しました

## 主な変更点
- meta タグの整理
- shortcode の追加
- ライブラリの変更
- RSS Feed の追加
- custom.css の読み込み機能
- シェアボタンの変更

### shortcode について
AMP へ対応と項目の追加しました。詳しくは [shortcode](#shortcode) へ

### ライブラリについて
- Font Awesome 5 へアップグレード
- highlight.js の削除

gist に対応したため highlight.js は廃止しました。

どうしてもシンタックスハイライトが使用したい場合は [公式の highlight](https://gohugo.io/content-management/syntax-highlighting/) を使用してください。
(ただしAMPページの場合エラーが発生します)

### RSS Feed
RSS Feed のテンプレートが存在してなかったため追加しました。

### custom.css
custom.css が存在する場合ファイルを読み込みます

### シェアボタンについて
シェアボタンのURLを更新し、非表示を可能にしました
各シェアボタンを非表示するには以下のようにすることで可能です

```toml
[Params]
# はてなブックマーク
socialShareHatena = false
# Twitter
socialShareTwitter = false
# Facebook
socialShareFacebook = false
# Google Plus
socialShareGoogleplus = false
# Pocket
socialSharePocket = false
# LINE
socialShareLine = false
```

シェアボタン自体を非表示にするには以下のようにすることで可能です

```toml
[Params]
socialShare = false
```

## shortcode
一部 shortcode は公式のものを使用しています。

### Gist
`{{< gist id="gistID" file="file" >}}`

### Twitter
`{{< twitter id >}}`

AMPに対応しました

### YouTube
`{{< youtube id >}}`
`{{< youtube id autoplay="true" >}}`

ID は `https://www.youtube.com/watch?v=` 以降の英数字です

AMPに対応しました