# minecraft:player_attacked_entity
このイベントは、プレイヤーがエンティティを攻撃するたびに発生します。

## パラメーター
|タイプ |名称  |説明 |
|---|---|---|
|Entity JS API Object |player |攻撃したプレイヤー|
|Entity JS API Object |attacked_entity |プレイヤーに攻撃されたエンティティ |

## プログラム例
```JavaScript
const system = server.registerSystem(0,0);

system.initialize = function() {
  this.listenForEvent ("minecraft:player_attacked_entity", (eventData) => this.removeAttackedEntity(eventData));
};

system.removeAttackedEntity = function(eventData) {
  const player = eventData.data.player;
  const attacked_entity = eventData.data.attacked_entity;

  // エンティティを削除
  this.destroyEntity(attacked_entity);
};
```
このプログラムは、プレイヤーがエンティティを殴ると、殴られたエンティティは削除され、ワールドから消滅するものです。
