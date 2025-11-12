# API Reference

Overview of primary surfaces. Detailed symbol docs can be generated with DocC.

## DiscordClient

- `init(token:)`
- `loginAndConnect(intents:)`
- `events` (AsyncSequence)
- `getCurrentUser()`
- `sendMessage(channelId:content:)`
- `on(_:handler:)`
- `rest` for REST endpoints

## REST Highlights

- Channels: send/edit/delete messages, embeds
- Interactions: create/list/delete commands (global/guild)
- Guilds: get/modify
- Webhooks: execute

## Sharding

- `ShardingGatewayManager`

## Models

- `User`, `Guild`, `Channel`, `Message`, `Role`, `Emoji`, etc.

Next: [Examples](./examples.md)
