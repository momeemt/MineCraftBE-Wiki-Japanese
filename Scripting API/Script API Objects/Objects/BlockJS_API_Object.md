# BlockJS API Object

|タイプ |名称  |説明 |
|---|---|---|
|String |\_\_type\_\_ |読み取り専用です。オブジェクトの種類を定義しています。「block」になります。|
|String |\_\_identifier\_\_|読み取り専用です。オブジェクトの識別子を表しています。例えば、岩盤ブロックの場合、「minecraft:bedrock」になります。 |
|JavaScript Object |ticking\_area |読み取り専用です。このブロックを取得するために使われたチッキングオブジェクトです。 |
|JavaScript Object |block\_position |読み取り専用です。これはブロックの座標であり、一意の識別子としても機能しています。<br><table><tr><th>タイプ</th><th>名称</th><th>説明</th></tr><tr><td>Integer</td><td>x</td><td>x座標</td></tr><tr><td>Integer</td><td>y</td><td>y座標</td></tr><tr><td>Integer</td><td>z</td><td>z座標</td></tr></table>|

[翻訳元](https://minecraft.gamepedia.com/index.php?title=Bedrock_Edition_beta_scripting_documentation&mobileaction=toggle_view_mobile#Block_JS_API_Object)
