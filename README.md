# Athsany – Decision Brain / Decision Memory System

[![Athsany Decision Brain Demo](https://img.youtube.com/vi/CZusGsMtbjM/maxresdefault.jpg)](https://youtu.be/CZusGsMtbjM)

> **Athsany** is a multi‑domain **decision brain layer** that turns messy real‑world information into concrete actions and evolving strategies – starting with multi‑asset financial markets and extendable to risk and industry scenarios.

---

## 0. What this repo is (and is not)

This repository publishes the **Athsany decision cockpit prototype and documentation**, not the full production engine.

**✅ Included in this repo**

- A live **decision cockpit demo** (GitHub Pages) built on static scenarios for HSI, XAUUSD, etc.  
- Athsany’s core decision model (conceptually):  
  `Information → Structured Views → Actions → Decision Memory`  
- High‑level documentation:
  - [`docs/architecture.md`](docs/architecture.md)
  - [`docs/decision-loop.md`](docs/decision-loop.md)
  - [`docs/decision-memory.md`](docs/decision-memory.md)
  - [`docs/use-cases.md`](docs/use-cases.md)

**❌ Not included in this repo**

- No live trading connectivity  
- No real‑time market data pipelines  
- No proprietary trading strategies or production decision‑engine code  
- No internal agent orchestration or confidential data sources

> This public repo focuses on **how Athsany expresses and structures decisions**, not the full details of how the internal engine operates.

---

## 1. What is Athsany?

**One‑line concept**

> Athsany is an always‑on **decision brain layer** that sits on top of your data and tools, continuously answering one question:  
> **“Given everything that is happening, how should our positions / resources be adjusted – and what did we do last time?”**

Athsany is **not** a chat AI, not a writing assistant, and not a simple trading‑signal bot.  
It is an always‑on **Decision Brain** that runs above events and data, turning real‑world signals into a continuous decision loop with long‑term memory and self‑correction.

Instead of waking an AI with prompts, Athsany continuously reads real‑world information (events, data, market movements, operational signals), maintains decision context over time, and keeps learning from how each decision actually plays out.

### 中文簡介

我們在建立的，不是聊天工具，而是一個可持續運作的「決策大腦層」：

- Athsany 不是 Chat AI，不是文書工具，也不是普通交易訊號系統。  
- 它是一個常駐在資訊與數據上層的 **Decision Brain**，可以將真實世界的訊號轉化為可持續運作的決策閉環，並透過 **decision memory** 持續自我修正。  
- 不是等你發問，而是長期自己讀資訊與數據，幫你想：今天應該怎樣調整盤面？上一次類似情況，我們是怎樣決定、結果如何？

---

## Investor‑focused overview

If you are an institutional investor or family office and want a structured overview of Athsany’s decision brain and architecture, please see:

👉 [`docs/investor_overview.md`](docs/investor_overview.md)

---

## 2. Live demo & video overview

### 🔍 Decision Cockpit Prototype

👉 **Open the Athsany Decision Cockpit Prototype**  
https://kei03kei-aiathsany.github.io/Athsany-decision-brain/

> Early prototype only – static scenarios, synthetic / simplified signals, **no live trading**.

### 🎥 29‑minute deep‑dive video

[![Athsany Decision Brain Demo](https://img.youtube.com/vi/CZusGsMtbjM/maxresdefault.jpg)](https://youtu.be/CZusGsMtbjM)

> This ~29‑minute walkthrough shows how Athsany turns real‑world information into a **structured decision process**, using financial markets as the first example scenario.

▶ More Athsany videos and live demos:  
https://www.youtube.com/channel/UCiMWr8y37j0DJpB4vBMFVGg

---

## 3. Decision loop – Information → Risk View → Strategy → Execution → Review

At the core of Athsany is a repeatable decision loop:

1. **Information / Events** – Ingest and interpret external information (data releases, market moves, domain‑specific signals, operational events, etc.).  
2. **Risk View** – Map this information into a structured view of exposure, timing, scenarios, and tail risks.  
3. **Strategy** – Generate or adjust strategies based on the current risk view and historical decision memory.  
4. **Execution** – Translate strategy into concrete actions (orders, hedges, alerts, resource shifts, monitoring rules).  
5. **Review & Memory** – Evaluate outcomes, measure deviation vs. intent, and write the results back into decision memory.

You can visualize this as a closed loop:

```text
Information → Risk View → Strategy → Execution → Review
                     ↑                          │
                     └──────── Decision Memory ─┘
```

Every cycle is tracked, versioned, and linked to its originating information context.

---

## 4. Decision Memory & Self‑Correction

Traditional tools focus on **signals at a single point in time**.  
Athsany focuses on **decision memory**:

- Logs every decision with its full context (information, risk view, chosen strategy).  
- Tracks outcomes and deviations (what actually happened vs. what was expected).  
- Stores post‑mortem reflections and corrections.  
- Feeds these back into the next round of decisions for similar patterns.

This allows the system to:

- Explain **why** a decision was made.  
- Identify **where** it was wrong.  
- Adjust **how** it responds next time – instead of repeating the same mistake.

### From gut feeling to readable memory

Most high‑stakes decisions today still depend on experience and gut feeling that live in people’s heads, chats, and meetings, but are hard to see, audit, or reuse as a system.

Athsany’s decision brain and decision memory are designed to **turn those tacit reactions into explicit, searchable decision history** — so that “how we usually handle this” becomes part of a readable, upgradeable decision infrastructure.

**中文說明**

很多關鍵決策其實來自經驗與直覺，散落在人腦裡、聊天室裡、會議紀錄裡，很難被看見或重用。  
Athsany 要做的，就是把這些「感覺上的做法」變成可閱讀、可查閱、可優化的決策基建。

---

## 5. Why Athsany cares about cascades

The world itself is not a straight line, and neither is a human life: from the moment you are born, you’re on a path of rises, falls, and sharp turns — some people ride a gentle slope, others a roller coaster.

Information and events are not straight lines either. They don’t “happen and disappear”; they cascade through time and space, like tectonic plates shifting into an earthquake, then into a tsunami. Financial markets and operational KPIs are simply the real‑time projection of these moving plates.

Athsany aims to be a JARVIS‑grade decision brain: not just watching price ticks or dashboards, but reading plate movements and cascades, then helping you choose paths that are less likely to blow up — and sometimes, let you shine.

**中文說明**

世界本身唔係一條直線，人生都唔係；事件與資訊都一樣，唔係「發生完就完」，而係會一路級聯，好似板塊移動引發地震，再由震央拉出海嘯。  
金融市場同企業營運數字，只係呢啲板塊移動嘅即時投影。  
Athsany 想做嘅，其實就係一個 JARVIS 級決策大腦：唔係淨係睇價位同 KPI，而係睇板塊點郁、級聯點發生，幫你喺呢啲唔直線嘅世界線入面，揀一條唔咁易翻車、甚至可以大放異彩嘅路。

---

## 6. Overview / Project scope

Athsany is a **decision support & risk management brain** for high‑uncertainty domains.

- Initial proving ground: multi‑asset financial markets (FX, indices, gold, futures, oil, equities, derivatives).  
- Extendable domains: risk (insurance, AML, real estate), and industry decisions (supply chain, energy, retail, operations, policy scenarios), etc.

Unlike typical Chat AI tools, Athsany:

- Does not wait for prompts to answer ad‑hoc questions.  
- Runs as a continuous layer that:  
  - digests information and events,  
  - maintains structured views of impact and risk,  
  - proposes actions under constraints,  
  - and writes everything into long‑term decision memory.

GitHub demo mainly shows Athsany as a **Decision Brain / decision cockpit** — how decisions are expressed and logged — not a full trading or operations system.

---

## 7. System view / Architecture (high‑level)

> This section is a **target system view**, to position Athsany as a piece of decision infrastructure.  
> Detailed production architecture and live deployment specifics remain internal.

From a high level, Athsany can be seen as three stacked layers:

```text
Information & Events
        │
        ▼
Analytics & Reasoning
        │
        ▼
Decision Engine & Memory
```

- **Information & Events**  
  - Structured data: prices, market data, customer / operational metrics, risk indicators.  
  - Unstructured signals: news, reports, internal notes, domain‑specific alerts – all aligned on a unified time axis.

- **Analytics & Reasoning**  
  - Feature engineering, regime detection, backtesting.  
  - Transform raw signals into structured views, scenarios, narratives and explanations.  
  - Produces numeric indicators and qualitative insights, but does not trade or act directly.

- **Decision Engine & Memory**  
  - Combines analytics and reasoning outputs to produce:  
    - Directional bias or stance (e.g. risk‑on / risk‑off, prioritize / de‑prioritize).  
    - Constraints and limits (risk budgets, exposure caps, priorities).  
    - Suggested actions and routing to different strategies / business units.  
  - Logs all decisions, actions and outcomes into decision memory for audit and learning.

For a more detailed breakdown, see: [`docs/architecture.md`](docs/architecture.md).

---

## 8. Use cases

The current demo uses HSI and XAUUSD as examples to illustrate:

- An information‑driven view vs. bare price‑only / technical charts.  
- Under major events, how to:  
  - move from “there is news” to a structured **world radar**,  
  - see which assets / segments are truly impacted, where flows might go,  
  - distinguish real impact vs. short‑term noise.

The same decision pattern can extend to:

- Multi‑asset portfolio risk management.  
- Insurance / AML / real‑estate risk intelligence.  
- Supply‑chain, energy, retail, operations and policy scenario planning.

More examples: [`docs/use-cases.md`](docs/use-cases.md)

> All public use‑cases are **conceptual / prototype scenarios** and do not constitute investment advice or performance guarantees.

---

## 9. Confidence levels (design concept)

To avoid over‑confident language on inherently uncertain outputs, Athsany introduces **confidence levels** for each decision suggestion:

- **High confidence**  
  - Historical hit‑rates are strong under similar regimes; ample samples.  
  - Allows clearer directional stance and more assertive sizing (subject to risk rules).

- **Medium confidence**  
  - Signals align but hit‑rates are moderate, or the market has partially priced in the information.  
  - Produces bias / tilt suggestions (lean long / lean short, modest adjustments).

- **Low confidence**  
  - Conflicting signals, sparse data, or regime shifts underway.  
  - Focuses on risk alerts and caps, rather than strong directional calls.

In future UI / API designs, each output will carry **confidence and risk labels**, so decision‑makers can instantly see “how hard” a suggestion is, and how much to lean on it.

---

## 10. Why Finance First, But Not Finance Only

Financial markets (e.g. major indices, FX and gold) are our most complete demonstration environment today, not the final scope of Athsany.

Finance is an ideal sandbox because it provides:

- Dense, high‑frequency information streams.  
- Clear outcomes and feedback loops.  
- Well‑defined notions of risk, position, and performance.

However, the core design of Athsany’s decision brain layer is **domain‑agnostic**.  
The same information → risk view → strategy → execution → review pattern can be applied to:

- Enterprise and operational risk management.  
- Supply chain and logistics decisions.  
- Security / incident response.  
- Any domain where information, risk, and long‑term decision evolution matter.

---

## 11. Market context – Why a decision brain layer matters

Predictive analytics, augmented analytics, and prediction markets already form a multi‑billion‑dollar space that is compounding towards the hundreds‑of‑billions. Most tools, however, still stop at **“more data and more charts”**.

Athsany sits one layer above as the **decision brain** — turning signals into concrete actions and persistent decision memory.  
The goal is to lower the barrier so that more people and institutions can actually *use* predictions to decide, accelerating adoption and the growth of the entire market.

**中文說明**

而家預測分析、增強分析同預測市場，加埋已經係一個幾百億美金、向千億級走嘅市場，但好多系統都停喺「出數據、出圖表」。  
Athsany 想做嘅係「決策大腦層」，幫呢啲訊號變成具體行動同決策記憶，令更多人同機構真係用預測嚟做決定，推動成個市場增長得更快。

---

## 12. Roadmap / Status & future

_Current status (will be updated as the system evolves):_

- ✅ Internal prototypes for information ingestion, decision logging, and memory structures.  
- ✅ Demo use‑cases on HSI futures and XAUUSD to validate the full loop.  
- 🚧 Building a more generalizable decision memory layer for non‑financial domains.  
- 🚧 Preparing public demos and documentation.  
- 🔭 Future: external API / SDK to embed Athsany as a decision brain layer into other systems.

---

## 13. Repository structure (current & planned)

This repository is focused on **concepts and architecture**, not full production code (yet).

```text
.
├── docs/
│   ├── architecture.md        # High-level system architecture
│   ├── decision-loop.md       # Information → Structured Views → Actions → Decision Memory
│   ├── decision-memory.md     # How decision memory is structured
│   └── use-cases.md           # Cross-domain applications of Athsany
├── examples/
│   ├── finance-hsi-xauusd/    # Finance demo scenarios
│   └── (future-domains)/      # Placeholders for non-finance demos
├── assets/
│   ├── decision-loop.png      # Visualization of the decision loop
│   └── athsany-diagrams.png   # Additional diagrams / thumbnails
└── README.md
```

As the project evolves, this repo can grow into:

- Public specifications of Athsany’s decision brain architecture.  
- Reference implementations and demo notebooks.  
- Domain‑specific examples beyond finance.

---

## 14. Disclaimer / 免責聲明

This repository focuses on **architecture, concepts, and non‑sensitive components** of the Athsany system.

- Production trading logic, proprietary strategy code and any confidential data sources are **not** included in this public repo.  
- The demo is an **early prototype** with **static scenarios and synthetic / simplified signals**, with **no live trading connectivity**.  
- Nothing in this repo or demo constitutes financial advice or a guarantee of performance.
