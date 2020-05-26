# bootstrap レイアウト編

## 目標時間

6時間〜8時間程度

## 目的

下記画像の内容を課題通りに実装する
<img src="img/index.png" alt="index" width="640" height="318">

## 実装

resources/views 下に index.blade.php を作成

index.blade.php
```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>test</title>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
  <style>
    body {
      background-color: #eee;
    }
    button {
      width: 100px;
    }
    .wrapper {
      width: 1100px;
    }
  </style>
</head>
<body>
  <div class="wrapper"></div>
</body>
</html>
```
testContoroller(書き換え)
```
/**
* index.blade.phpを返す
*/
public function index()
{
    return view('index');
}
```

これで準備は完了です。

### 補足
- linkタグでbootstrapを読み込んでいます。ですが、まだclassしか読み込んでいませんのでbootstrapの全ての機能が使えるわけではありません。（今回の実装には問題ありません。）
- 自作のcssを読み込むときはbootstrapのlinkタグより下に記述します。
（今回はbootstrapの課題ですので、使わないでください）

## 課題

下記の条件に従いbootstrapを用いて実装してください。

- 画像（index.png）の通りにformを作成して下さい。(imgフォルダの中にもあります。)
- 各項目それぞれのnameは`familyName`,`firstName`,`e-mail`,`sex`,`age`,`note`とし、性別以外はidもnameと同じで結構です。性別はidを`male`,`female`としてください。
- 各ボタンのidは`submit-btn`,`clear-btn`,`temp-btn`,`disabled-btn`としてください。
- typeはそれぞれ適切なものにしてください。
- 送信ボタンの色は`primary`です。
- クリアボタンを押すとformの内容がリセットされるようにしてください。色は`secondary`です。
- テンプレボタンの色は`success`です。
- 操作不能ボタンの色は`danger`です。
- padding,marginについて
    - 指示がある場所以外に、指定する必要がある場合は`0.5rem`を指定してください

すこし見慣れない指定があると思いますが、Bootstrapの使い方を把握すればわかるはずです。しっかり調べましょう。

完成したらjs.mdに進んでください。