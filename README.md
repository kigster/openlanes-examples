# OpenLanes examples

Starting points for [OpenLanes](https://github.com/kigster/openlanes): small app skeletons with a goals document and a few seed plans, ready for the factory to build.

Copy one out, `cd` into it, and start the factory:

```bash
ol new --example rust-logtail ~/src/logtail   # copies the template, runs git init and ol init -y
cd ~/src/logtail
ol start
```

Do not run `ol start` inside this checkout: the agents would build into the template itself. Every template carries a `.openlanes-template` marker, and `ol start` refuses where it finds one.

## Templates

| Template | Stack | App | Status |
| --- | --- | --- | --- |
| `macos-clipboard` | Swift, SwiftUI, SwiftPM | Clipboard history in the menu bar | planned |
| `rust-logtail` | Rust | `logtail`: a CLI that follows and filters JSON logs | planned |
| `rails-habits` | Ruby on Rails | Habit tracker with streaks | planned |
| `astro-blog` | Astro, TypeScript, static output | A markdown blog: posts, tags, RSS | planned |

`ol new --example` with no name lists the folders this repository holds.

## What a template contains

```
<template>/
  README.md                what the app is, what to install, how to build and run it
  .openlanes-template      marker; holds the minimum openlanes version
  .plans/
    APPLICATION.md         what it is, goals, non-goals, stack, what done looks like
    BACKLOG.md             candidates that are not plans yet (optional)
    001.00━━⚪━━❯<slug>/    two or three seed plans, each with a spec.md
  <a skeleton that builds>
```

The full walk from an empty directory to `ol start` is [`docs/STARTING-AN-APP.md`](https://github.com/kigster/openlanes/blob/main/docs/STARTING-AN-APP.md) in the OpenLanes repository.

## Contributing

Templates for other stacks are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md) for what a template must pass.
