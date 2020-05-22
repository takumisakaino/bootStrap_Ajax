# bootstrap js基礎編

## 目標時間

4時間〜6時間程度

## 目的

次章に向けての準備をする  
前章で作成したページに動きをつける

## 導入

index.blade.php  
下記追記を行う

```
// 略
  </style>
  <script src="https://code.jquery.com/jquery-3.4.1.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>{{-- 追記 --}}
  <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>{{-- 追記 --}}
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>{{-- 追記 --}}
</head>
// 略
```

jsファイルの作成
- public下にjsフォルダを作成
- その中にscript.jsを作成し`alert('ok');`を記述。

jsファイルを読み込む
- 3つ目のscriptタグの下に`<script src="{{ asset('js/script.js') }}"></script>`を記述してブラウザをリロード
- ブラウザでアラートが表示されたら先程のjsファイルからalert()は消し、以下を記述

script.js
```
// HTMLが読み込まれた時に処理したい内容はこの中に
$(function(){

});
// 外には変数定義や関数定義を
```

## 補足

- 公式のプラグインはスリム版でAjaxが使えませんので今回はフルバージョンを読み込んでいます。
- asset()はlaravelのpublicディレクトリ以下のファイルを指定してパスを取得します

## 課題

色々調べてやってみましょう。

- 問一　送信ボタンをクリックしたら入力値をすべて取得しひとつずつconsoleに表示する。
- 問二　テンプレボタンをクリックすると下記内容が各入力欄に入力される
    - 姓　gizumo
    - 名　華子
    - メール　gizumo@gmail.com
    - 性別　女性
    - 年齢　20~29
    - 備考　hondaに勤めている
- 問三　操作不能ボタンをクリックすると操作不能ボタン以外のすべての項目が操作不能になりもう一度押すと解除される。


完成したらphp&Ajax.mdに進んでください