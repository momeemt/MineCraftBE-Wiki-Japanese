# minecraft:client_entered_world
このイベントは、プレイヤーがワールドに参加するたびに発生します。

## パラメーター
|タイプ |名称  |説明 |
|---|---|---|
|Entity JS API Object |player |参加したプレイヤー|

## プログラム例
```JavaScript
const system = server.registerSystem(0,0);

system.initialize = function() {
  this.listenForEvent ("minecraft:client_entered_world", (eventData) => this.onJoinPlayer(eventData));
};

system.onJoinPlayer = function(eventData) {
  const player = eventData.data.player;

  // プレイヤーの名前
  const player_name = this.getComponent(player, "minecraft:nameable").data.name;

  // アクションバーに表示
  let ExecuteEventData = this.createEventData("minecraft:execute_command");
  ExecuteEventData.data.command = `/title @a actionbar ${player_name} が参加しました。`;
  this.broadcastEvent("minecraft:execute_command", ExecuteEventData);
};
```

このプログラムは、ワールドに参加したプレイヤーの名前をアクションバーに表示するものです。
