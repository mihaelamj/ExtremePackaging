# ExtremePackaging

Demo project for modular Swift app architecture using the Extreme Packaging
approach.

The repo shows how to start a multi-platform Swift app with app targets kept
thin and most logic isolated into Swift packages. It is intentionally small:
the value is the staged structure, not a finished product.

## Core Idea

- Put reusable code in Swift packages.
- Keep iOS and macOS app targets as platform shells.
- Share contracts instead of concrete implementations.
- Add packages in stages so the architecture stays understandable.
- Use SwiftLint and SwiftFormat from the beginning.

## Project Structure

```text
ExtremePackaging/
├── Apps/
│   ├── iOSApp/
│   └── macOSApp/
├── Packages/
│   ├── AppFeature/
│   └── SharedModels/
└── Main.xcworkspace
```

## Stages

Each branch captures a checkpoint in the setup:

1. `stage/01-init-packages`: initial package structure.
2. `stage/02-workspace`: workspace integration.
3. `stage/03-apps-added`: iOS and macOS app targets consuming packages.

```bash
git checkout stage/03-apps-added
```

## Why It Exists

This is a reference repo for conversations about modular Swift apps. It is
useful when you want to show the mechanical setup for package-first app
architecture without mixing it into a larger real product.

## Status

Public demo/reference repo. Not a framework and not an app template with a
stable API.
