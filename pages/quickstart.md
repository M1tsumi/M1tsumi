# Quickstart

A minimal bot that connects with intents and processes events using AsyncSequence.

```swift
import SwiftDisc

@main
struct BotMain {
    static func main() async {
        let token = ProcessInfo.processInfo.environment["DISCORD_TOKEN"] ?? "YOUR_BOT_TOKEN"
        let client = DiscordClient(token: token)

        do {
            try await client.loginAndConnect(intents: [
                .guilds,
                .guildMessages,
                .messageContent // privileged; enable in Developer Portal if needed
            ])

            for await event in client.events {
                switch event {
                case .ready(let info):
                    print("✅ Connected as: \(info.user.username)")
                case .messageCreate(let message):
                    if message.content == "!ping" {
                        try await client.sendMessage(channelId: message.channel_id, content: "pong!")
                    }
                default:
                    break
                }
            }
        } catch {
            print("❌ Error: \(error)")
        }
    }
}
```

- Use environment variables for secrets.
- Prefer minimal intents for better performance.

Next: [Core Concepts](./core-concepts.md)
