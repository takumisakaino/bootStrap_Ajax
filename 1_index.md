# 下準備

## 目標時間

30分〜1時間程度

## 目的

- 作業開始の準備を整え、`hello word`を表示させる


## hello world の表示

README.mdが終わってない方は先にそちらをやってください。

### controllerの作成

- laravel ディレクトリで、`php artisan make:controller testController`を実行し作成
- メソッドの作成
    - testControllerに下記コードを記入

```
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
/indexにgetメソッドでアクセスされたら、testControllerのindexメソッドを実行するという意味

ブラウザで`http://127.0.0.1:8000/index`にアクセスしhello worldが表示出来たら成功です。

ここまで出来たらOKです。

次はhtml.mdです。