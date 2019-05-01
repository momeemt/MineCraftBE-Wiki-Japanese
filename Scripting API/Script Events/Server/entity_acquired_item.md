# minecraft:entity_acquired_item
このイベントは、エンティティがアイテムを取得するたびに発生します。

## パラメーター
|タイプ |名称  |説明 |
|---|---|---|
|Entity JS API Object |entity |アイテムを取得したエンティティ|
|ItemStack JS API Object |item_stack |取得したアイテム |
|String |acquisition_method |エンティティがアイテムを取得した方法 |
|Integer |acquired_amount |エンティティが取得したアイテムの個数 |
|Entity JS API Object |secondary_entity |アイテムを取得する際にそのアイテムに影響を与えたエンティティ(存在しない場合もあります)。|

注: secondary_entity の例として、村人との交易があります。この場合、「entity」プロパティがプレイヤーに、「secondary_entity」プロパティが村人になります。

## プログラム例
```JavaScript
const system = server.registerSystem(0,0);

system.initialize = function() {
  this.listenForEvent ("minecraft:entity_acquired_item", (eventData) => this.getItemProperty(eventData));
};

system.getItemProperty = function(eventData) {
  const entity = eventData.data.entity;
  const item_stack = eventData.data.item_stack;
  const amount = eventData.data.acquired_amount;

  // アイテム識別子を取り出す
  const item = item_stack.item;

  // display_chat_eventイベント
  let BroadcastEventData = this.createEventData("minecraft:display_chat_event");
  BroadcastEventData.data.message = `${entity} がアイテムを取得しました！取得したアイテムは、${item}で、${amount}個です！`;
  this.broadcastEvent("minecraft:display_chat_event", BroadcastEventData);
};
```

このプログラムは、アイテムを拾った際に誰が何を何個拾ったかをチャットで流すものです。
