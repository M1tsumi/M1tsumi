# Production Deployment

## Health and monitoring

- Periodic `healthCheck()` for all shards
- `shardHealth(id:)` to inspect a specific shard
- Structured logs; integrate with swift-log and your observability stack

## Configuration

- Shard count: `.automatic` to start; scale as needed
- Intents: minimum required; enable privileged in Developer Portal if needed
- Backoff/retry: built-in reconnects with heartbeat ACK tracking

## Secrets

- Use environment variables (e.g., `DISCORD_TOKEN`)
- Never commit secrets to source control

## Rollouts

- Graceful restarts per shard using `restartShard(_:)`
- Staggered reconnects for large bots
