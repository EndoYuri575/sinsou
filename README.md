# 脱出ゲーム 真相ページ

合言葉を入力するとQRコードが表示され、それを読み取ると「真相」ページが開きます。

## ファイル構成

| ファイル | 役割 |
|---|---|
| `index.html` | 合言葉の入力ページ（参加者が最初に開く） |
| `shinsou.html` | 真相ページ（QRコードの読み取り先） |
| `style.css` | 2ページ共通の見た目 |
| `qrcode.js` | QRコードを作るプログラム（MIT License） |
| `本文.txt` | 真相ページの文章メモ |

この5つは同じ階層に置いたまま使ってください。

## 公開後のURL

- 合言葉ページ：`https://ユーザー名.github.io/リポジトリ名/`
- 真相ページ　：`https://ユーザー名.github.io/リポジトリ名/shinsou.html`

QRコードのリンク先は自動で決まるため、URLを手で書きこむ必要はありません。

## 設定を変える

`index.html` の下のほう、`【設定】` と書かれた場所にあります。

```javascript
const PASSWORD   = "きどう";        // 合言葉
const TRUTH_PAGE = "shinsou.html";  // QRの読み取り先
```

真相ページの文章は `shinsou.html` の `<p>` 〜 `</p>` の中にあります。

## 合言葉の判定

次のちがいは、すべて正解になります。

- スペースの有無
- 大文字・小文字
- 全角・半角の英数字
- カタカナ・ひらがな（「キドウ」でも「きどう」でも可）

「軌道」と漢字で入力した場合は不正解になります。

> ⚠️ 合言葉はページのソースに書かれているため、ソースを見れば分かります。
> 演出のための仕掛けとしてお使いください。

## ライセンス

`qrcode.js` は Kazuhiko Arase 氏による [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator)（MIT License）です。
