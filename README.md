## Zohaib Qamar

I build the layer that makes AI agents safe to let loose on real systems: who's allowed to
do what, who approved it, and whether the agent told the truth about what happened.

### What I've built

**[Zori (HiveOS)](https://github.com/zbs-ops/zori-hive-os)**: a governed execution layer for
enterprise AI. Every AI action is a task in a database-enforced state machine, with tenant
isolation through Postgres row-level security, sandboxed Docker workers, and an append-only
audit pipeline. NestJS, Postgres, Redis. **550+ tests**, including 19 integration suites
against real Postgres and Docker.

**[agent-governance](https://github.com/zbs-ops/agent-governance)**: a control plane between
agents and the things they can break. Policy checks, human approval for risky actions, and a
tamper-evident audit log. Approvals are authenticated per reviewer, an agent can't approve
its own action, and an adversarial eval suite runs on every change.
**[Live demo](https://agent-governance-theta.vercel.app)**

**[tool-truth](https://github.com/zbs-ops/tool-truth)**: catches agents stating facts their
tools never returned. Tested on 660 real customer-service conversations from τ-bench: the
first version failed on real data, and after fixing it, it caught agents inventing a round
trip and a store website. [The write-up](https://github.com/zbs-ops/tool-truth/blob/main/study/RESULTS.md)
includes the parts that went badly.

**[gate-bypass-bench](https://github.com/zbs-ops/gate-bypass-bench)**: measures how often an
agent's command blocklist can be talked around. Blocklists were bypassed 31–78% of the time;
an allowlist held at 0%. Builds on recent research whose authors released no code.

**[durastream](https://github.com/zbs-ops/durastream)**: a durable, replay-safe event log
built from the storage layer up, with checksums and retention.

### Open source

Contributing upstream to AI evaluation tooling, e.g.
[Giskard #2883](https://github.com/Giskard-AI/giskard-oss/pull/2883): enforce secret scanning in CI.

### How I work

Tests first, honest numbers, and a README that says what doesn't work yet. I build with an AI
coding assistant as a pair programmer: I decide what gets built, review every change, and own
what ships.

[LinkedIn](https://www.linkedin.com/in/zohaib-qamar-qwertyu/)
