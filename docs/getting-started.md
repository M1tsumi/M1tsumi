# Getting Started

This guide helps you set up your first SwiftDisc project.

## Prerequisites

- Xcode 15+ or Swift 5.9+
- A Discord bot token
- Basic Swift knowledge

## Create a new project

1. Create a new Swift Package or App project.
2. Add SwiftDisc as a dependency (see [Installation](./installation.md)).
3. Ensure your token is set via `DISCORD_TOKEN` environment variable.

## Your first client

```swift
import SwiftDisc

@main
struct BotMain {
    static func main() async {
        let token = ProcessInfo.processInfo.environment["DISCORD_TOKEN"] ?? "YOUR_BOT_TOKEN"
        let client = DiscordClient(token: token)
        do {
            try await client.loginAndConnect(intents: [.guilds, .guildMessages])
            for await _ in client.events { /* handle events */ }
        } catch {
            print("Error: \(error)")
        }
    }
}
```

Next: [Installation](./installation.md)
