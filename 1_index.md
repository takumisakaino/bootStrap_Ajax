## 導入

- Laravelをインストール
```
composer create-project laravel/laravel --prefer-dist なまえ
```
- laravelディレクトリにターミナル上で移動し`php artisan serve`を実行しサーバーを起動する
- `http://127.0.0.1:8000` にアクセスし、Laravelのtopが表示出来たら成功です。

## hello world　の表示

### controllerの作成

- `php artisan make:controller testController`を実行し作成
- メソッドの作成
    - testControllerに下記コードを記入

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
Route::get('index', 'testController@index')->name('test.index');
```
indexにgetメソッドでアクセスされたら、testControllerのindexメソッドを実行するという意味

`http://127.0.0.1:8000/index`にアクセスしhello worldが表示出来たら成功です。

ここまで出来たらOKです。

次はhtml.mdです。