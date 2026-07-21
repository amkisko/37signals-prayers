# thirtyseven shared prayers

Central distribution point for unofficial Rails agent guidance distilled from public 37signals codebases (Campfire, Fizzy) and DHH review patterns.

> **Unofficial.** Community packages based on public code and discussions — not affiliated with or endorsed by 37signals.

Packages here are reusable inference input for [pray](https://github.com/kiskolabs/pray). Product overview: [pray.kisko.dev](https://pray.kisko.dev).

## Install pray

```sh
cargo install --git https://github.com/kiskolabs/pray --locked pray
```

## Use these prayers in a project

From your project root:

```sh
pray init
```

Local sibling checkout:

```prayfile
source "thirtyseven", path: "../37signals-prayers/prayers"

target :agents do
  output "AGENTS.md"
  skills ".agents/skills"
end

agent "thirtyseven/rails-best-practices-core", "~> 0.1", source: "thirtyseven", exports: ["skill"]
agent "thirtyseven/dhh", "~> 0.1", source: "thirtyseven", exports: ["skill"]

render mode: :managed, conflict: :fail, churn: :minimal
```

After this repository is published, consumers can use a git source:

```prayfile
source "thirtyseven", git: "https://github.com/amkisko/37signals-prayers", distribution: "prayers"
agent "thirtyseven/rails-best-practices-core", "~> 0.1", source: "thirtyseven", exports: ["skill"]
```

Resolve and render:

```sh
pray install
pray plan
pray apply
pray verify
```

## Publish or update a package

```sh
make publish
make release
```

## Package catalog

| Package | Type | Summary |
|---------|------|---------|
| `thirtyseven/getting-started` | fragment | Install pray and wire a consumer |
| `thirtyseven/overview` | fragment | Catalog of thirtyseven packages |
| `thirtyseven/rails-best-practices-core` | skill | Architecture, modeling, REST, authorization |
| `thirtyseven/rails-hotwire-realtime` | skill | Turbo, Stimulus, ActionCable, presence |
| `thirtyseven/rails-jobs` | skill | Active Job, Solid Queue, retries |
| `thirtyseven/rails-migrations` | skill | Safe schema changes and rollouts |
| `thirtyseven/rails-security-multitenancy` | skill | Tenancy, auth, SSRF, rate limits |
| `thirtyseven/rails-testing` | skill | Minitest and fixtures |
| `thirtyseven/rails-webhooks` | skill | Outbound delivery and signing |
| `thirtyseven/dhh` | skill | DHH-style review (`/dhh`) |

Long-form topic notes for humans: [`docs/guide/`](docs/guide/).

## Layout

```text
prayers/                  # distribution root (index, metadata, artifacts)
packages/                 # package sources (.prayspec + content)
docs/guide/               # long-form human reference (not packaged by default)
Prayfile                  # publisher manifest for this repo
Makefile                  # install, publish, release, serve, clean
```

## Links

- [pray CLI](https://github.com/kiskolabs/pray)
- [pray.kisko.dev](https://pray.kisko.dev)
- Upstream skills origin: [marckohlbrugge/37signals-skills](https://github.com/marckohlbrugge/37signals-skills)
