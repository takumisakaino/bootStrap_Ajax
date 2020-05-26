# bootStrap&Ajax課題

慣れてない人でも4〜5日を想定しているような簡単な内容になっています。慣れている人は2〜3日を目標にやってみましょう！


## 導入（目標時間:30分〜1時間）

- Laravelをインストール
```
composer create-project laravel/laravel --prefer-dist なまえ
```
- laravel ディレクトリで、`php artisan make:controller testController`を実行し作成
- `http://127.0.0.1:8000` にアクセスし、Laravelのtopが表示出来たら成功です。

## hello world　の表示

### controllerの作成

- `php artisan make:controller TestController`を実行し作成
- メソッドの作成
    - TestControllerに下記コードを記入

```
/**
* 文字列hello worldを返すという意味
*/
public function index()
{
    return 'hello world';
}
```

### ルーティングの作成
- routes/web.php に記述
    - 下記コードを記入
```
Route::get('test', 'TestController@index')->name('test');
```
/indexにgetメソッドでアクセスされたら、testControllerのindexメソッドを実行するという意味

ブラウザで`http://127.0.0.1:8000/index`にアクセスしhello worldが表示出来たら成功です。

ここまで出来たらOKです。

次はhtml.mdです。
