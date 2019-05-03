# hourly_clock_time
現在時間と0から24000までの数値を比較します。
[Minecraft における1日](https://minecraft-ja.gamepedia.com/%E6%98%BC%E5%A4%9C%E3%82%B5%E3%82%A4%E3%82%AF%E3%83%AB#.E7.8F.BE.E5.AE.9F.E6.99.82.E9.96.93.E3.81.8B.E3.82.89_Minecraft_.E3.81.A7.E3.81.AE.E6.99.82.E9.96.93)

## パラメーター
| タイプ | 名称 | デフォルト値 | 説明 |
|---|---|---|---|
| String | subject | self | このテストの条件対象。(オプション)<br><table><tr><th>オプション</th><th>説明</th></tr><tr><td>self</td><td>テストを呼び出したエンティティ、オブジェクト</td></tr><tr><td>other</td><td>イベント対話中で、テストを呼び出していないエンティティ、オブジェクト</td></tr><tr><td>parent</td><td>テストを呼び出したエンティティ、オブジェクトの親状態にあるエンティティ、オブジェクト</td></tr><tr><td>player</td><td>イベント対話に関与したプレイヤー</td></tr><tr><td>target</td><td>現在ターゲットになっているエンティティ、オブジェクト</td></tr></table> |
| String | operator | equals | <br> <table><tr><th>オプション</th><th>説明</th></tr><tr><td>>=</td><td>value以上であればtrueを返します</td></tr><tr><td>equals</td><td>valueと等しければtrueを返します</td></tr><tr><td><></td><td>valueと等しくなければtrueを返します</td></tr><tr><td>==</td><td>valueと等しければtrueを返します</td></tr><tr><td>=</td><td>valueと等しければtrueを返します</td></tr><tr><td>not</td><td>valueと等しくなければtrueを返します</td></tr><tr><td><</td><td>valueより小さければtrueを返します</td></tr><tr><td>!=</td><td>valueと等しくなければtrueを返します</td></tr><tr><td>></td><td>valueより大きければtrueを返します</td></tr><tr><td><=</td><td>value以下であればtrueを返します</td></tr></table>|
| Integer | value |  | 0から24000までの数値 (必須) |

## コード例
```json
{ "test": "hourly_clock_time", "subject": "self", "operator": "equals", "value": "0" }
```

これは、現在時間とvalueが一致する時のみにtrueを返すフィルタです。  
デフォルト値を使うことで、省略して記述できます。

```json
{ "test": "hourly_clock_time", "value": "0" }
```

[翻訳元](https://minecraft.gamepedia.com/Bedrock_Edition_entity_components_documentation#hourly_clock_time)
