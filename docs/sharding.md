# Sharding

SwiftDisc provides a high-level `ShardingGatewayManager` for production-grade sharding.

## Basic usage

```swift
let manager = await ShardingGatewayManager(
    token: token,
    configuration: .init(shardCount: .automatic),
    intents: [.guilds, .guildMessages]
)
try await manager.connect()

for await sharded in manager.events {
    switch sharded.event {
    case .ready(let info):
        print("READY on shard \(sharded.shardId): \(info.user.username)")
    default: break
    }
}
```

## Best practices

- Start with `.automatic` shard count
- Monitor shard health in production (`healthCheck()`, `shardHealth(id:)`)
- Use `.staggered(interval:)` for very large bots
- `restartShard(_:)` to recover a problem shard without full restart

## Troubleshooting

- Failed shard connects → verify token/network/Discord status
- Uneven guild distribution → restart affected shard; ensure automatic shard count
