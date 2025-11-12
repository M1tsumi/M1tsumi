# Examples

## Ping bot (prefix)

```swift
for await event in client.events {
    if case .messageCreate(let m) = event, m.content == "!ping" {
        try await client.sendMessage(channelId: m.channel_id, content: "pong!")
    }
}
```

## Commands bot (prefix help)

```swift
switch event {
case .messageCreate(let m) where m.content.hasPrefix("!help"):
    try await client.sendMessage(channelId: m.channel_id, content: "Commands: !ping, !help")
default: break
}
```

## Slash command hello

```swift
// See Examples/SlashBot.swift in the repo for a full flow
// Create a global command, then handle interactionCreate
for await event in client.events {
    if case .interactionCreate(let i) = event, i.isCommand("/hello") {
        try await i.respond("Hello there! ")
    }
}

Next: [FAQ](./faq.md)
