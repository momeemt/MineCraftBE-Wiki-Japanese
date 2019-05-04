# has_biome_tag  
テストの条件対象が居るバイオームに、特定のタグがある場合trueを返します。
  
# パラメーター

<dl><dd><table class="wikitable">
<tbody><tr>
<th>タイプ</th>
<th>名称</th>
<th>デフォルト値</th>
<th>説明
</th></tr>
<tr>
<td>String
</td>
<td>subject
</td>
<td>self
</td>
<td>このテストの条件対象。(オプション)
<dl><dd><table class="wikitable">
<tbody><tr>
<th>オプション</th>
<th>説明
</th></tr>
<tr>
<td>self
</td>
<td>テストを呼び出したエンティティ、オブジェクト
</td></tr>
<tr>
<td>other
</td>
<td>イベント対話中で、テストを呼び出していないエンティティ、オブジェクト
</td></tr>
<tr>
<td>parent
</td>
<td>テストを呼び出したエンティティ、オブジェクトの親状態にあるエンティティ、オブジェクト
</td></tr>
<tr>
<td>player
</td>
<td>イベント対話に関与したプレイヤー
</td></tr>
<tr>
<td>target
</td>
<td>現在ターゲットになっているエンティティ、オブジェクト
</td></tr></tbody></table></dd></dl>
</td></tr>
<tr>
<td>String
</td>
<td>operator
</td>
<td>equals
</td>
<td>値を比較するための演算子。(オプション)
<dl><dd><table class="wikitable">
<tbody><tr>
<th>オプション</th>
<th>説明
</th></tr>
<tr>
<td>&gt;=
</td>
<td>value以上であればtrueを返します
</td></tr>
<tr>
<td>equals
</td>
<td>valueと等しければtrueを返します
</td></tr>
<tr>
<td>&lt;&gt;
</td>
<td>valueと等しくなければtrueを返します
</td></tr>
<tr>
<td>==
</td>
<td>valueと等しければtrueを返します
</td></tr>
<tr>
<td>=
</td>
<td>valueと等しければtrueを返します
</td></tr>
<tr>
<td>not
</td>
<td>valueと等しくなければtrueを返します
</td></tr>
<tr>
<td>&lt;
</td>
<td>valueより小さければtrueを返します
</td></tr>
<tr>
<td>!=
</td>
<td>valueと等しくなければtrueを返します
</td></tr>
<tr>
<td>&gt;
</td>
<td>valueより大きければtrueを返します
</td></tr>
<tr>
<td>&lt;=
</td>
<td>value以下であればtrueを返します
</td></tr></tbody></table></dd></dl>
</td></tr>
<tr>
<td>String
</td>
<td>value
</td>
<td>
</td>
<td>検証するタグ(必須)
</td></tr></tbody></table></dd></dl>


# サンプルコード 
```json
{ "test": "has_biome_tag", "subject": "self", "operator": "equals", "value": " " }
```
これは、self(テストを呼び出したエンティティ、オブジェクト)がいるバイオームに、  
`　`(value)がある際にtrueを返すフィルタです。  
デフォルト値を使うことで、省略して記述できます。  
```json
{ "test": "has_biome_tag", "value": " " }
```  
[翻訳元](https://minecraft.gamepedia.com/Bedrock_Edition_entity_components_documentation#has_biome_tag)  
