# TRAMPOLINE FLIP

長押しだけで宙返りする、競技用トランポリンのブラウザゲーム（HTML5 / Canvas、外部ライブラリなし）。

## ファイル
| ファイル | 用途 |
|---|---|
| index.html | ゲーム本体（これ1つで動く） |
| favicon.ico / favicon.svg | ブラウザのタブのアイコン |
| apple-touch-icon.png | iPhoneでホーム画面に追加したときのアイコン |
| icon-192.png / icon-512.png | Androidのホーム画面用アイコン |
| manifest.webmanifest | ホーム画面に追加したときの名前・色・アイコンの設定 |
| og-image.png | LINE・X などでURLを共有したときに出る画像 |

## 公開手順（GitHub → Netlify）
1. GitHubで新しいリポジトリを作り、このフォルダの中身をすべてアップロード（フォルダごとではなく、中のファイルを直下に置く）
2. Netlifyで「Add new site → Import an existing project」→ GitHubのリポジトリを選択
3. Build command は空欄、Publish directory も空欄（またはルート）のままデプロイ

## 公開後にやること
LINEやXで共有したときに画像を出すため、`index.html` の次の2か所を公開URLに書き換えてください。

```html
<meta property="og:image" content="https://（公開URL）/og-image.png">
<meta property="og:url" content="https://（公開URL）/">
```

## 操作
- ジャンプは自動。長押し中だけ回転、離すと体が開いて回転が止まる
- 最初の技から連続10本の合計点で勝負。演技中は前方系・後方系が交互
- 10本の後は自動でストレートジャンプ → ビタ止めで演技終了
- 左下の ♪ で消音
