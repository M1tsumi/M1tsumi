# Windows Notes

- Swift toolchain for Windows required; ensure `swift` is on PATH
- Uses Foundation's URLSession WebSocket; if unavailable, gateway will report WebSocket unsupported
- A dedicated Windows WebSocket adapter is planned; track the CHANGELOG for updates

## Running on Windows

- Set `DISCORD_TOKEN` in your environment
- Run via `swift run` or your chosen process manager

## Troubleshooting

- No events: check intents and privileged message content
- Frequent disconnects: inspect network stability; automatic reconnects are enabled
