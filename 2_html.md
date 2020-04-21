# HTML（目標時間:6時間〜8時間）

## 導入

resources/views 下に index.blade.php を作成

index.blade.php
```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>test</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
  <script src="https://code.jquery.com/jquery-3.4.1.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
</head>
<body style="background-color: #eee;">


</body>
</html>
```
testContoroller(書き換え)
```
/**
* top画面を表示する
*/
public function index()
{
    return view('index');
}
```

- jsファイルの作成
    - public下にjsフォルダを作成
    - その中にscript.jsを作成し`alert('ok');`を記述。

- jsファイルを読み込む
    - 3つ目のscriptタグの下に`<script src="{{ asset('js/script.js') }}"></script>`を記述してブラウザをリロード
        - asset()はlaravelのpublic下のファイルを指定してパスを取得します
    - 読み込みが確認出来たらalert()は消す。

これで準備は完了です。

### 補足
- linkとscript×3でbootstrapを読み込んでいます。
- 公式のプラグインはスリム版でAjaxが使えませんので今回はフルバージョンを読み込んでいます。
- 自作のcssを読み込むときはbootstrapのlinkタグより下に記述します。


## HTML、bootstrap練習

いよいよ実践です。下記の条件に従いbootstrapを用いて実装してください。px指定のあるところに関しては直接スタイルをあてて結構です。

- index.pngの通りにformを作成して下さい。
- コンテンツ幅は1100pxです。
- ボタンの大きさは100pxです。
- footerのborderの色は#ced4daです。
- 各項目それぞれのnameは`familyName`,`firstName`,`e-mail`,`sex`,`age`,`note`とし、性別以外はidもnameと同じで結構です。性別はidを`male`,`female`としてください。
- typeはそれぞれ適切なものにしてください。
- 各ボタンのidは`submit-btn`,`clear-btn`,`temp-btn`,`disabled-btn`としてください。
- 送信ボタンの色は`primary`です。
- クリアボタンを押すとformの内容がリセットされるようにしてください。色は`secondary`です。
- テンプレボタンの色は`success`です。
- 操作不能ボタンの色は`danger`です。
- bootstrapではpaddingやmarginが５段階で指定できるようになっています。
    - 基本的に２を指定してください
    - コンテンツの上からの距離は５、フッターコンテンツは４を指定してください

すこし見慣れない指定があると思いますが、Bootstrapの使い方を把握すればわかるはずです。しっかり調べましょう。

完成したらjs.mdに進んでください。