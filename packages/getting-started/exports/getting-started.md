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
