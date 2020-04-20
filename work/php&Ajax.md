# PHP & Ajax

## ゴール

送信ボタンを押したらformの値をコントローラーに送り、動的なHTMLを返し、帰ってきたHTMLを表示し疑似的なリストを作成する。

## 狙い

- 動的なHTMLを作成できるようになる
- Ajaxの使い方を学ぶ

## 準備

- php
    - ルーティング
        - web.phpに追加する。
    - list.blade.phpを作成する。
    - controller
        - list.blade.phpを返すように記述する

- html 
    - formタグの下にid="testList"を持つulタグを記述する
```
<ul id="testList" class="mt-5"></ul>
```
- formタグに、action、method、idを追加する
    - 上記でweb.phpに記述したルートに従い記入する


- 動的なHTMLを作成する。下記静的html
```
<li class="mb-1">
    <div class="">
        <div class="p-2"></div>
        <div class="p-2"></div>
        <div class="p-2"></div>
        <div class="p-2"></div>
    </div>
    <div class="mt-1" style="display: none;">
        <p class="p-2 m-0"></p> // ここに備考
    </div>
</li>
```

## 課題

下記に従い処理を実装してください

- 送信ボタンを押したとき、上記で作成したメソッドに対してAjax通信を行いformの内容をcontrollerに送信する。
- 受け取った値を使い動的なHTMLをreturnする。
- Ajax成功時帰ってきたHTMLをulに表示する
    - Ajax.pngを参考
- 表示したliをクリックするとそのliに対応する備考がスライドダウンし、もう一度クリックするとスライドアップする
    - Ajax_after.pngを参考

完成したら終了です。お疲れさまでした。


