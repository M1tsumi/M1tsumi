# Advanced Features

## Scheduled Events
```swift
let ev = try await client.createGuildScheduledEvent(
  guildId: guildId,
  channelId: voiceChannelId,
  entityType: .voice,
  name: "Community Meetup",
  scheduledStartTimeISO8601: "2026-01-10T18:00:00Z",
  description: "Monthly chat"
)
```

## Stage Instances
```swift
let stage = try await client.createStageInstance(
  channelId: stageChannelId,
  topic: "Q&A with the dev team",
  privacyLevel: 2
)
```

## Auto Moderation
```swift
let rule = try await client.createAutoModerationRule(
  guildId: guildId,
  name: "Block Spam Links",
  eventType: 1,
  triggerType: 3,
  actions: [ .init(type: 1, metadata: nil) ]
)
```

## Audit Logs
```swift
let logs = try await client.getGuildAuditLog(guildId: guildId, actionType: 20, limit: 50)
```

## Stickers
```swift
let stickers = try await client.listGuildStickers(guildId: guildId)
```

## Forum Channels
```swift
let thread = try await client.createForumThread(
  channelId: forumChannelId,
  name: "How do I use SwiftDisc?",
  content: "I'm trying to build a bot...",
  autoArchiveDuration: 1440
)
```
