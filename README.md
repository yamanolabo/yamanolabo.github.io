# やまのらぼ サイト

赤茶を基調にした、静的サイトです。ビルドは不要で、そのまま公開できます。

## ファイル

| ファイル | 中身 |
|---|---|
| `index.html` | トップ（表紙 / About / Works / Contact） |
| `movie-shelf.html` | MOVIE Shelf の紹介ページ |
| `privacy.html` | プライバシーポリシー（**全アプリ共通**）。Play Console に出す URL はこのページです |
| `style.css` | 共通スタイル。色は先頭の `:root` にまとまっています |
| `google3fc0984e73b06454.html` | Google Search Console の所有権確認ファイル（触らないこと） |
| `play-listing.md` | Play Console の提出文面（サイトには不要。公開したくなければ消してください） |

前のサイトにあった `work-01.html` 〜 `work-04.html` は、テンプレートの架空の作例だったため削除しました。

## GitHub Pages で公開する

1. GitHub でリポジトリを作る（公開／`yamanolabo.github.io` という名前にすると `https://yamanolabo.github.io/` になります）
2. このフォルダの中身をそのまま置いて push する
3. Settings → Pages → Source を `Deploy from a branch`、Branch を `main` / `(root)` にする
4. 数分待つと公開されます

公開後のプライバシーポリシーの URL は次の形です。Play Console にはこれを入れます。

```
https://<ユーザー名>.github.io/privacy.html
```

リポジトリ名を `yamanolabo.github.io` 以外にした場合は、そのリポジトリ名が間に入ります。

```
https://<ユーザー名>.github.io/<リポジトリ名>/privacy.html
```

## 色を変えたいとき

`style.css` の先頭にまとまっています。ここだけ触れば全ページに反映されます。

```css
--board:      #d9c9ae;   /* いちばん外側の台紙 */
--paper:      #f4ece0;   /* 本体の紙 */
--paper-lit:  #fbf6ed;   /* カードなど、明るい紙 */
--ink:        #2b211c;   /* 本文 */
--brand:      #7b3a2c;   /* 赤茶（基調色） */
--brand-deep: #4f241b;   /* 濃い赤茶。見出しなど */
--brand-lit:  #a45a44;   /* 明るい赤茶 */
--brass:      #9c7b4a;   /* 真鍮。節番号の小札 */
```

## アプリを増やすとき

`privacy.html` は最初から複数アプリを想定した書き方にしてあります。増えたときは2か所を足すだけです。

1. 「1. 対象となるアプリ」の表に一行追加（アプリ名・対応・権限・課金）
2. 「9. アプリごとの補足」にそのアプリの節を追加

本文（収集しない／端末内で完結／課金は Google Play が処理、など）は共通なので触る必要がありません。
URL も `privacy.html` のまま使い回せるので、Play Console の入力を全アプリで揃えられます。
更新したら、冒頭の「最終更新日」を変えてください。

## 作品を増やすとき

`index.html` の Works の中にある `<a class="work">…</a>` を複製し、リンク先と文言を差し替えます。
紹介ページは `movie-shelf.html` をコピーして作るのが早いです。

## 画像について

このサイトは写真を1枚も使っていません。ロゴマークと本棚の見立ては、すべて SVG と CSS で描いています。
差し替えたくなったら、`movie-shelf.html` の `.shelf` の中身を `<img>` に置き換えてください。
