# is_daytime
日中、太陽が出ている時にtrueを返します。  

## パラメーター
|タイプ |名称  |デフォルト値 |説明 |
|---|---|---|---|
|String |subject |self |このテストの条件対象。(オプション) <br><table><tr><th>オプション</th><th>説明</th></tr><tr><td>self</td><td>テストを呼び出したエンティティ、オブジェクト</td></tr><tr><td>other</td><td>イベント対話中で、テストを呼び出していないエンティティ、オブジェクト</td></tr><tr><td>parent</td><td>テストを呼び出したエンティティ、オブジェクトの親状態にあるエンティティ、オブジェクト</td></tr><tr><td>player</td><td>イベント対話に関与したプレイヤー</td></tr><tr><td>target</td><td>現在ターゲットになっているエンティティ、オブジェクト</td></tr></table>|
|String |operator |equals |値を比較するための演算子。(オプション)<br> <table><tr><th>オプション</th><th>説明</th></tr><tr><td>>=</td><td>value以上であればtrueを返します</td></tr><tr><td>equals</td><td>valueと等しければtrueを返します</td></tr><tr><td><></td><td>valueと等しくなければtrueを返します</td></tr><tr><td>==</td><td>valueと等しければtrueを返します</td></tr><tr><td>=</td><td>valueと等しければtrueを返します</td></tr><tr><td>not</td><td>valueと等しくなければtrueを返します</td></tr><tr><td><</td><td>valueより小さければtrueを返します</td></tr><tr><td>!=</td><td>valueと等しくなければtrueを返します</td></tr><tr><td>></td><td>valueより大きければtrueを返します</td></tr><tr><td><=</td><td>value以下であればtrueを返します</td></tr></table>|
|Boolean |value |true |true,false (オプション)|

## コード例
```json
{ "test": "is_daytime", "subject": "self", "operator": "equals", "value": "true" }
```

これは、日中だった際にtrueを返すフィルタです。  
デフォルト値を使うことで、省略して記述できます。

```json
{ "test": "is_daytime" }
```
