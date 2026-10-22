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

**[TYDE](https://github.com/shobhitsrivastava2023/TYDE)** &nbsp;`TypeScript` `Next.js` `Electron`

A keyboard-driven explainer canvas for recording technical videos. The script streams in word by word like an AI chat response, but the presenter controls the pace: each keypress reveals the next beat, and nothing moves on its own. The stage is a free-form canvas rather than a slide template. Text, images, diagrams, hand-drawn arrows and KaTeX math sit wherever you place them.

- Scripts are plain markdown with directives, editable in a text editor or visually in the app (drag, resize, retype). Both write to the same file.
- Arrows are rendered with rough.js, anchor to elements and re-route as things move. Their wobble is seeded, so every take renders identically.
- Excalidraw SVG exports are inlined, recoloured to the theme, and can reveal one shape at a time.
- A camera follows content as it grows and supports per-beat pan and zoom. It is replayed from step zero on every render, so stepping back and forth always lands on the same frame.
- Layout is computed up front and only opacity changes during streaming, so text never reflows mid-sentence.
- The stage is a fixed 1920x1080 canvas with no UI chrome, ready to capture in OBS. Ships as a Windows installer.

<img src="https://raw.githubusercontent.com/shobhitsrivastava2023/TYDE/main/docs/screenshots/stage.png" alt="TYDE stage mid-presentation" width="720" />

**[CodeStage](https://github.com/shobhitsrivastava2023/codestage)** &nbsp;`Rust` `Tauri v2` `React` `TypeScript`

A presentation tool for code: Keynote, but every slide is a step in a program. You write code in sequential steps and CodeStage animates the transitions between them at the token level. Unchanged code slides into place, new code fades in, removed code fades out.

- Built on Tauri v2 with a Rust backend and a React frontend, using Shiki and shiki-magic-move for highlighting and token animation, and CodeMirror 6 for editing.
- Line highlighting with dimming, and a camera that follows the relevant lines in long files.
- Present mode opens a borderless fullscreen window for recording, plus a separate presenter window with notes, a next-step preview and a timer.
- Projects are JSON files saved atomically with autosave, so a crash never corrupts work.
- 13 bundled themes, offline fonts, and 16:9 or 9:16 canvases for long-form videos and shorts. Ships as Windows installers (.exe and .msi).

<img src="https://raw.githubusercontent.com/shobhitsrivastava2023/codestage/main/docs/screenshot.png" alt="CodeStage editor" width="720" />

---

### Also

[EndTest](https://github.com/shobhitsrivastava2023/EndTests): API capacity planning with staged load tests, runtime telemetry and SLA checks. &nbsp;|&nbsp; [LEXEL](https://github.com/shobhitsrivastava2023/lexel): voice platform with TTS, voice cloning and an LLM-as-judge quality loop.

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
