# minecraft:entity_carried_item_changed
このイベントは、エンティティがアイテムを持ち替えるたびに発生します。

## パラメーター
|タイプ |名称  |説明 |
|---|---|---|
|Entity JS API Object |entity |持ち替えたエンティティ|
|ItemStack JS API Object |previous_carried_item |持ち替える前に持っていたアイテム |
|ItemStack JS API Object |carried_item |今手に持っているアイテム |

## プログラム例
```JavaScript
const system = server.registerSystem(0,0);

system.initialize = function() {
  this.listenForEvent ("minecraft:entity_carried_item_changed", (eventData) => this.deleteItemTNT(eventData));
};

system.deleteItemTNT = function(eventData) {
  if (eventData.data.entity === "minecraft:player"){
    const player = eventData.data.entity;
    const item = eventData.data.carried_item.item;

    // プレイヤーの名前
    const player_name = this.getComponent(player, "minecraft:nameable").data.name;

    if (item === "minecraft:tnt") {
      // TNTを没収
      let ExecuteEventData = this.createEventData("minecraft:execute_command");
      ExecuteEventData.data.command = `/clear ${player_name}  tnt`;
      this.broadcastEvent("minecraft:execute_command", ExecuteEventData);
    }

  }else {
    return;
  }
};
```

このプログラムは、プレイヤーがTNTを持った場合に削除するものです。
