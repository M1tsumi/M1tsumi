# Installation

SwiftDisc is distributed via Swift Package Manager (SPM).

## Package.swift

Add this to your `dependencies` and target:

```swift
dependencies: [
    .package(url: "https://github.com/M1tsumi/SwiftDisc.git", from: "0.5.0")
],

targets: [
    .executableTarget(
        name: "MyBot",
        dependencies: [
            .product(name: "SwiftDisc", package: "SwiftDisc")
        ]
    )
]
```

## Xcode UI

- File → Add Packages…
- Enter repo URL: `https://github.com/M1tsumi/SwiftDisc`
- Version rule: Up to Next Major from 0.5.0
- Add the `SwiftDisc` product to your target

Next: [Quickstart](./quickstart.md)
