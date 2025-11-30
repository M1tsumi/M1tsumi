# Hey, I'm M1tsumi

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-quefep-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/6nS2KqxQtj)
[![GitHub followers](https://img.shields.io/github/followers/M1tsumi?style=for-the-badge&logo=github)](https://github.com/M1tsumi)
[![Website](https://img.shields.io/badge/Docs-quefep.uk-blue?style=for-the-badge)](https://quefep.uk)

</div>

## About Me

Systems programmer specializing in high-performance developer tooling across Swift, Objective-C, Zig, and Rust. I build production-ready libraries focused on type safety, performance, and good developer experience.

```swift
let developer = Developer(
    username: "M1tsumi",
    discord: "quefep",
    languages: ["Swift", "Objective-C", "Zig", "Rust"],
    focus: ["Discord APIs", "Concurrency", "Systems Programming"]
)
```

---

## Projects

### Discord API Wrappers

<table>
<tr>
<td width="33%" valign="top">

#### SwiftDisc
Modern Discord API wrapper for Swift

```swift
let client = DiscordClient(token: token)
try await client.connect()
```

- Discord API v10 support
- Native async/await
- Type-safe API
- Cross-platform (iOS, macOS, tvOS, watchOS, Windows)
- Automatic rate limiting
- Zero dependencies

[Repository](https://github.com/M1tsumi/SwiftDisc) | [Documentation](https://quefep.uk)

</td>
<td width="33%" valign="top">

#### Caelum
Discord API wrapper for Objective-C

```objc
DiscordClient *client = 
    [[DiscordClient alloc] initWithToken:token];
[client connect];
```

- Complete Discord API coverage
- Swift interoperability
- Memory-safe implementation
- CocoaPods & SPM support
- Battle-tested in production

[Repository](https://github.com/M1tsumi/Caelum)

</td>
<td width="33%" valign="top">

#### Zignal
High-performance Discord API for Zig

```zig
var client = try zignal.Client.init(
    allocator, .{ .token = token }
);
try client.connect();
```

- Discord API v10 (175 endpoints)
- Gateway support (56 events)
- Voice channels with audio
- 20x faster startup than Python
- 4x lower memory usage
- Zero dependencies

[Repository](https://github.com/M1tsumi/Zignal) | [Documentation](https://docs.zignal.dev)

</td>
</tr>
</table>

### Systems Programming

<table>
<tr>
<td width="50%" valign="top">

#### VelocityX
Lock-free concurrent data structures for Rust

```rust
use velocityx::mpmc::Queue;

let queue: Queue<i32> = Queue::new(1024);
queue.push(value).unwrap();
let item = queue.pop();
```

- MPMC queues and concurrent hashmaps
- Zero-lock atomic operations
- Thread-safe by design
- Comprehensive benchmarks

Available on [crates.io](https://crates.io/crates/velocityx)

</td>
<td width="50%" valign="top">

#### Other Work

**Arena-b** - High-performance arena allocator for Zig

**ZeroProto** - Zero-copy protocol buffer implementation

**AeroSocket** - Lightweight WebSocket library

</td>
</tr>
</table>

---

## Tech Stack

<div align="center">

![Swift](https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white)
![Objective-C](https://img.shields.io/badge/Objective--C-438EFF?style=for-the-badge&logo=apple&logoColor=white)
![Zig](https://img.shields.io/badge/Zig-F7A41D?style=for-the-badge&logo=zig&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Discord API](https://img.shields.io/badge/Discord_API-5865F2?style=for-the-badge&logo=discord&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Xcode](https://img.shields.io/badge/Xcode-147EFB?style=for-the-badge&logo=xcode&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

---

## Current Work

- Expanding Discord API coverage in SwiftDisc, Caelum, and Zignal
- Performance optimization for VelocityX
- Improving documentation across all projects
- Maintaining compatibility with Discord API updates
- Research into lock-free algorithms and concurrent data structures

---

## Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=M1tsumi&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" height="170"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=M1tsumi&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" height="170"/>

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=M1tsumi&theme=tokyonight&hide_border=true)

</div>

---

## Contributing

Open to collaboration and contributions on any projects. Feel free to:

- Star repositories you find useful
- Report bugs or request features
- Submit pull requests
- Join the Discord community

<div align="center">

[![Join Discord](https://invidget.switchblade.xyz/6nS2KqxQtj)](https://discord.gg/6nS2KqxQtj)

</div>

---

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=M1tsumi&color=5865F2&style=flat-square&label=Profile+Views)

</div>
