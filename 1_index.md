# hello worldを表示

## 目標時間

30分〜1時間程度

## 目的

- コントローラーの作成、ルーティングの方法を覚える


## 実装

※README.mdが終わってない方は先にそちらをやってください。

### controllerの作成

- 用意したlaravelプロジェクトがあるディレクトリで、`php artisan make:controller TestController`を実行
- メソッドの作成
    - TestControllerに下記コードを記入

```php
public function index()
{
    return 'hello world';
}
```

### ルーティングの作成
- routes/web.phpに下記コードを記入
```php
Route::get('index', 'TestController@index')->name('index');
```
`/index`にgetメソッドでアクセスされたら、TestControllerのindexメソッドを実行するという意味。

ブラウザで`http://127.0.0.1:8000/index`にアクセスしhello worldが表示出来たら成功です。

ここまで出来たらOKです。

次は2_html.mdです。
