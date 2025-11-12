# Core Concepts

- **DiscordClient**
  Central entrypoint handling REST and Gateway.

- **Models**
  Type-safe representations of Discord entities (User, Guild, Channel, Message, etc.).

- **Gateway**
  Real-time events over WebSocket. Manages identify, heartbeats, resume, and intents.

- **Intents**
  Select which events you receive. Configure minimally for performance.

- **Events (AsyncSequence)**
  Consume `client.events` with `for await` and switch over event enums.

- **REST & Rate Limiting**
  JSON encode/decode, structured errors, and automatic retries with per-route buckets.

- **Logging**
  Prints structured logs by default; integrate with swift-log if desired.

- **Sharding**
  `ShardingGatewayManager` for production bots requiring multiple shards.

- **Architecture Layers**
  DiscordClient -> Gateway -> Intents -> Events (AsyncSequence) -> REST & Rate Limiting -> Logging -> Sharding

Next: [Gateway & Events](./gateway-and-events.md)
