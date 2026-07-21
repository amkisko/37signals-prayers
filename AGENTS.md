<!-- pray:0 ignore-comments -->

# Agent context

Do not edit managed blocks in `AGENTS.md` or provisioned files under `.agents/`.
To change shared guidance, update `Prayfile` and run `pray install`.

## Shared instructions

<!-- pray:5c45d63b -->
## Shared prayers (thirtyseven)

This project can use [pray](https://github.com/kiskolabs/pray) to install Rails guidance packages derived from public 37signals patterns (unofficial; not affiliated with 37signals).

Install the CLI:

```sh
cargo install --git https://github.com/kiskolabs/pray --locked pray
```

Initialize or update managed input:

```sh
pray install
pray plan
pray apply
pray verify
```

Declare dependencies in `Prayfile`. Do not edit managed spans in `AGENTS.md` or `.agents/skills/`.

Distribution source: [amkisko/37signals-prayers](https://github.com/amkisko/37signals-prayers).
Product docs: [pray.kisko.dev](https://pray.kisko.dev).
<!-- pray:5c45d63b -->

<!-- pray:5e3e3529 -->
## thirtyseven Rails prayers

Unofficial Rails agent skills distilled from public 37signals codebases (Campfire, Fizzy) and DHH review patterns. Not affiliated with or endorsed by 37signals.

Install as folder skills via pray (export name `skill` on each package):

- `thirtyseven/rails-best-practices-core` — baseline architecture, modeling, REST, authorization
- `thirtyseven/rails-hotwire-realtime` — Turbo, Stimulus, ActionCable, presence
- `thirtyseven/rails-jobs` — Active Job, Solid Queue, retries
- `thirtyseven/rails-migrations` — safe schema changes and rollouts
- `thirtyseven/rails-security-multitenancy` — tenancy, auth, SSRF, rate limits
- `thirtyseven/rails-testing` — Minitest and fixtures
- `thirtyseven/rails-webhooks` — outbound delivery and signing
- `thirtyseven/dhh` — DHH-style review (`/dhh`)

Long-form topic notes live in this repository under `docs/guide/` and are not rendered into agent input by default.
<!-- pray:5e3e3529 -->
