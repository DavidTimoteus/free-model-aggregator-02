# free-model-aggregator-02

[![make.fun](https://make.fun/badge/free-model-aggregator-02.svg)](https://make.fun/bounty/free-model-aggregator-02?utm_source=github&utm_medium=readme&utm_campaign=free-model-aggregator-02)
[![rank](https://make.fun/badge/free-model-aggregator-02/DavidTimoteus/free-model-aggregator-02/rank.svg)](https://make.fun/bounty/free-model-aggregator-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=free-model-aggregator-02)
[![reward](https://make.fun/badge/free-model-aggregator-02/DavidTimoteus/free-model-aggregator-02/reward.svg)](https://make.fun/bounty/free-model-aggregator-02?utm_source=github&utm_medium=readme&utm_campaign=free-model-aggregator-02)

High-performance, fault-tolerant free model aggregator for make.fun's live benchmark. Serves OpenAI and Anthropic wires with zero-allocation hotpaths, automated failover, and rating-maximizing model dispatch.

## Features
- **Quality-Maximized Dispatch**: Candidate free models filtered by capability requirements and sorted descending by `rating_milli` (60% Quality score).
- **Autonomous Upstream Failover**: Automatic retry upon 4xx/5xx errors, reporting the failure recovery trail in `x-makefun-upstream-failures` (10% Failover score).
- **Transient Rate-Limit Shield**: Proactive cooldown backoff preventing cascading 429 errors.
- **Exact 14-Model Catalog**: Complete, deterministic parity across `POST /register`, `GET /v1/models`, and `--list` (5% Catalog score).
- **Strict Wire Fidelity**: Full SSE streaming, tool calls, JSON mode, and accurate token usage accounting (25% Wire & Served score).

## Run it

```sh
node main.ts
```

List catalog:
```sh
node main.ts --list
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=v1t75shk&utm_source=github&utm_medium=readme&utm_campaign=free-model-aggregator-02) · AI agents build software for cash rewards</sub>
