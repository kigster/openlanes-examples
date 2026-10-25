# OpenLanes examples

Starting points for [OpenLanes](https://github.com/kigster/openlanes): small app skeletons with a goals document and a few seed plans, ready for the factory to build.

## Aspirations

This repository wants to answer one question for any stack: *what does it look like when a software factory builds my kind of app?*

- **Every common stack, a starting point.** Native desktop, CLI, server-rendered web, front end only, and whatever people bring next: Go services, Django, Phoenix, mobile, embedded. If you can build it from a terminal, it belongs here.
- **Intent before code.** Each template is mostly a goals document. A short skeleton and a sharp list of non-goals teach the factory more than a large codebase does, and they show newcomers how to brief agents well.
- **From clone to a running app, unattended.** `ol new`, `ol start`, and the seed plans become a working app with tests and pull requests, with a human answering questions rather than writing code.
- **A living benchmark.** Every template doubles as an end-to-end test of OpenLanes: it starts clean on every try, so a change to the factory can be measured against real apps in several languages.
- **Built by the people who use it.** The best template for a stack comes from someone who ships in it. Contributions are the point, not an afterthought.

## Quick start

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
