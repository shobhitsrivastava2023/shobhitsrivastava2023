## Shobhit Srivastava

Software engineer working on backend and distributed systems, developer tools, and applied AI.

I like building the hard part myself before reaching for a library: a consensus algorithm, a job orchestrator, a benchmarking harness. I care about systems that are testable, that fail predictably, and whose performance claims come with the numbers behind them.

Most recently I owned end-to-end payment integration at Skaya for a consumer platform with 30-40K users. Since 2023 I have shipped 24+ production projects for clients in the UK and India, from requirements and system design through deployment and on-call support.

[shobhitsrivastava.com](https://www.shobhitsrivastava.com) &nbsp;|&nbsp; [LinkedIn](https://linkedin.com/in/shobhit-srivastava-s1323) &nbsp;|&nbsp; shobhitsrivastava729@gmail.com

---

### Selected work

**[RaftKV](https://github.com/shobhitsrivastava2023/raftkv)** &nbsp;`Java 21` `gRPC` `Docker`
A distributed key-value store built on Raft, implemented from the paper with no consensus library. It covers leader election, log replication, durable storage with crash recovery, snapshots with InstallSnapshot, linearizable reads through ReadIndex, and exactly-once client writes. The node talks to the network, disk and clock only through interfaces, so the test suite runs a full 5-node cluster deterministically in one thread. It then pushes that cluster through 1,000 seeded fault scenarios (partitions, message loss and reordering, crashes) and checks the Raft safety properties after every event.

**[NonLinear Workflows](https://github.com/shobhitsrivastava2023/Non-Linear-WorkFlows-)** &nbsp;`TypeScript` `Node.js` `Redis` `PostgreSQL`
An orchestration backend for multi-step AI agents with 300+ third-party tool integrations. It has a Redis-backed shared state store for step coordination, background job queues, rate limiting, webhook ingestion, OAuth 2.0 token lifecycle management, and retry orchestration for failed steps.

**[EndTest](https://github.com/shobhitsrivastava2023/EndTests)** &nbsp;`TypeScript` `Node.js`
An API capacity-planning tool. It runs staged load scenarios (baseline, ramp, saturation, soak) while sampling process CPU, memory and event-loop lag. It evaluates p95/p99 latency and error-rate SLAs and reports a safe request rate, the likely bottleneck, and a starting estimate for cloud instance sizing.

**[LEXEL](https://github.com/shobhitsrivastava2023/lexel)** &nbsp;`Next.js` `tRPC` `Prisma` `PostgreSQL` `Cloudflare R2`
A voice platform built on Chatterbox TTS, with voice cloning, live transcription and a real-time streaming voice agent. Output quality is enforced by an automated loop: an LLM acting as an adversarial judge scores each synthesis and re-runs it with corrected parameters until it meets the quality threshold.

---

### Developer tools

Two desktop apps I built for my own technical videos. Both ship Windows installers.

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/shobhitsrivastava2023/codestage"><img src="https://raw.githubusercontent.com/shobhitsrivastava2023/codestage/main/docs/screenshot.png" alt="CodeStage editor" /></a>
<br/><b><a href="https://github.com/shobhitsrivastava2023/codestage">CodeStage</a></b> &nbsp;<code>Tauri v2</code> <code>Rust</code> <code>React</code>
<br/>A presentation tool for code. You write code in steps, and it animates the token-level changes between them for tutorial recordings.
</td>
<td width="50%" valign="top">
<a href="https://github.com/shobhitsrivastava2023/TYDE"><img src="https://raw.githubusercontent.com/shobhitsrivastava2023/TYDE/main/docs/screenshots/stage.png" alt="TYDE stage" /></a>
<br/><b><a href="https://github.com/shobhitsrivastava2023/TYDE">TYDE</a></b> &nbsp;<code>Next.js</code> <code>Electron</code>
<br/>A keyboard-driven explainer canvas. Scripts stream in beat by beat on a free-form stage of text, diagrams, hand-drawn arrows and math.
</td>
</tr>
</table>

---

### Tools I work with

| | |
|---|---|
| Languages | Java 17/21, TypeScript, Python, SQL, Rust |
| Backend | Spring Boot, Node.js, FastAPI, gRPC, tRPC, Next.js |
| Data and infrastructure | PostgreSQL, Redis, Kafka, Prisma, Docker, Kubernetes, GitHub Actions, Cloudflare R2 |
| Concurrency and JVM | java.util.concurrent, virtual threads, CompletableFuture, JFR, async-profiler |
| AI | LLM integration, agent orchestration, LLM-as-judge evaluation, RAG, speech pipelines |

B.Tech in Information Technology, Manipal University Jaipur.
