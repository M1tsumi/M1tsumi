# Gateway & Events

## Connecting

```swift
let client = DiscordClient(token: token)
try await client.loginAndConnect(intents: [.guilds, .guildMessages])
```

## Subscribing to events

```swift
for await event in client.events {
    switch event {
    case .ready(let info):
        print("READY: \(info.user.username)")
    case .messageCreate(let message):
        print("#\(message.channel_id): \(message.author.username): \(message.content)")
    default:
        break
    }
}
```

## Common events

- `ready`
- `messageCreate`
- `interactionCreate`
- `guildCreate`
- `guildMemberAdd`

## Reconnect logic

- Identify/Heartbeat with ACK tracking.
- Automatic resume and retry with backoff on disconnect.

Next: [API Reference](./api-reference.md)
