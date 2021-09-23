# 📜 async-crashdump-debugging Charter

The goal of this initiative is to provide tools that simplify debugging crashdumps of async Rust programs.

## Proposal

In particular the initiative strives to provide:

- Debugger plugins for GDB and WinDbg/CDB that help with
  - finding executors from various runtimes (future-rs, Tokio, smol)
  - listing tasks currently being owned by a given executor
  - mapping a task object to the source definition it represents
  - creating logical stack traces that shows dependencies between tasks and resources
- A test framework for debugger plugins
- A guide for writing plugins for other debuggers
- A guide for forking and extending debugging plugins in order to support custom, proprietary executor runtimes
- Integration with tokio-console (?)

Debugging a crashdump of an async Rust program requires both intimiate knowledge of
executor runtime internals and a certain level of expertise in using debuggers.
It is the goal of this initiative to provide a toolbox that makes this task less daunting.
A good portion of the more difficult debugger interactions can be automated via plugins.

## Membership

| Role | Github | Zulip |
| ---  | ------ | ----- |
| [Owner] | [michaelwoerister](https://github.com/michaelwoerister) | mw |
<!-- | [Liaison] | [ghost](https://github.com/ghost) | -->

[Owner]: https://lang-team.rust-lang.org/initiatives/process/roles/owner.html
<!-- [Liaison]: https://lang-team.rust-lang.org/initiatives/process/roles/liaison.html -->
