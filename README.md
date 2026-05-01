# Athsany – Decision Brain / Decision Memory System

[![Athsany Decision Brain Demo](https://img.youtube.com/vi/CZusGsMtbjM/maxresdefault.jpg)](https://youtu.be/CZusGsMtbjM)

> **Athsany** is a multidomain *decision brain* for high‑uncertainty decisions, starting from multi‑asset financial markets and extendable to risk and industry scenarios.

---

## 0. What this repo is (and is not)

This repository publishes the **Athsany decision cockpit prototype and documentation**, not the full production engine.

**✅ Included in this repo**

- A live **decision cockpit demo** (GitHub Pages) built on static scenarios for HSI, XAUUSD, etc.  
- Athsany’s core decision model:  
  `Scenario → Event Cascade → Decision Output → Decision Memory`  
- High‑level documentation:
  - [`docs/architecture.md`](docs/architecture.md)
  - [`docs/decision-loop.md`](docs/decision-loop.md)
  - [`docs/decision-memory.md`](docs/decision-memory.md)
  - [`docs/use-cases.md`](docs/use-cases.md)

**❌ Not included in this repo**

- No live trading connectivity  
- No real‑time market data pipelines  
- No proprietary trading strategies or production decision engine code  
- No internal agent orchestration or confidential data sources

> This public repo focuses on **how Athsany expresses and structures decisions**, not the full details of how the internal engine operates.

---

## 1. What is Athsany?

Athsany is not a chat AI, not a writing assistant, and not a simple trading signal bot.  
It is an always‑on **Decision Brain** that sits on top of events and data, turning real‑world signals into a continuous decision loop with long‑term memory and self‑correction.

Instead of waking an AI with prompts, Athsany continuously reads real‑world events, data, and market movements, maintains decision context over time, and keeps learning from how each decision actually plays out.

**中文簡介**

我們在建立的，不是聊天工具，而是一個可持續運作的決策大腦層。  
Athsany 不是 Chat AI，不是文書工具，也不是普通交易訊號系統。它是一個常駐在事件與數據上層的決策大腦（Decision Brain），可以將真實世界的事件轉化為可持續運作的決策閉環，並透過長期 decision memory 持續自我修正。

---

## 2. Live demo & video overview

### 🔍 Decision Cockpit Prototype

👉 [Open the Athsany Decision Cockpit Prototype](https://kei03kei-aiathsany.github.io/Athsany-decision-brain/)

> Early prototype only – static scenarios, synthetic / simplified signals, **no live trading**.

### 🎥 29‑minute deep‑dive video

[![Athsany Decision Brain Demo](https://img.youtube.com/vi/CZusGsMtbjM/maxresdefault.jpg)](https://youtu.be/CZusGsMtbjM)

> This ~29‑minute walkthrough shows how Athsany turns real‑world events into a **structured decision process** – from *event* → *understanding* → *navigation* → *strategy*, using financial markets as the first example scenario.

▶ More Athsany videos and live demos:  
[https://www.youtube.com/channel/UCiMWr8y37j0DJpB4vBMFVGg](https://www.youtube.com/channel/UCiMWr8y37j0DJpB4vBMFVGg)

---

## 3. Decision Loop – Event → Risk → Strategy → Execution → Review

At the core of Athsany is a repeatable decision loop:

1. **Event** – Ingest and interpret external events (data releases, market moves, domain‑specific signals, etc.).  
2. **Risk** – Map each event into a structured risk view (exposure, timing, scenarios, tail risks).  
3. **Strategy** – Generate or adjust strategies based on the current risk state and historical decision memory.  
4. **Execution** – Translate strategy into concrete actions (orders, hedges, alerts, monitoring rules).  
5. **Review** – Evaluate outcomes, measure deviation vs. intent, and write the results back into decision memory.

You can visualize this as a closed loop:

```text
Event → Risk → Strategy → Execution → Review → (back into memory and next decisions)
```

Every cycle is tracked, versioned, and linked to its originating events.

---

## 4. Decision Memory & Self‑Correction

Traditional tools focus on signals at a single point in time.  
Athsany focuses on **decision memory**:

- Logs every decision with its full context (events, risk view, chosen strategy).  
- Tracks outcomes and deviations (what actually happened vs. what was expected).  
- Stores post‑mortem reflections and corrections.  
- Feeds these back into the next round of decisions for similar event patterns.

This allows the system to:

- Explain **why** a decision was made.  
- Identify **where** it was wrong.  
- Adjust **how** it responds next time, instead of repeating the same mistake.

### From gut feeling to readable memory

Most high‑stakes decisions today still depend on experience and gut feeling that live in people’s heads, chats, and meetings, but are hard to see, audit, or reuse as a system.

Athsany’s decision brain and decision memory are designed to **turn those tacit reactions into explicit, searchable decision history** – so that “how we usually handle this” becomes part of a readable, upgradeable decision infrastructure.

**中文說明**  
很多關鍵決策其實來自經驗與直覺，散落在人腦裡、聊天室裡、會議紀錄裡，很難被看見或重用。Athsany 要做的，就是把這些「感覺上的做法」變成可閱讀、可查閱、可優化的決策基建。

---

## 5. Overview / 專案簡介

Athsany 是一個聚焦 **決策支援與風險管理** 的多領域智能大腦，用於處理高不確定性場景：

- 核心戰場：多資產金融市場（外匯、指數、黃金、期貨、原油、正股與衍生品）
- 可延伸戰場：風險（保險、AML、房地產）與產業決策（供應鏈、能源、零售、企業營運、政策情景推演）等

同一般 Chat AI 不同，Athsany：

- 唔係等你發問先臨急臨忙答問題  
- 而係長期自己讀事件同數據，將複雜世界收斂成：
  - 可理解嘅 **事件結構**
  - 可執行嘅 **市場導航**
  - 可累積嘅 **決策記憶**

GitHub demo 主要展示嘅，是 Athsany 作為 **Decision Brain / decision cockpit** 點樣表達決策，而唔係完整交易系統。

---

## 6. System view / 架構視角（high‑level）

> 本節係 **目標系統視角**，方便理解 Athsany 屬於邊一類 decision infrastructure。  
> 真實 production 架構與實盤細節仍屬內部資產，未在本 repo 完整公開。

從系統角度，Athsany 可以概括為四層：

```text
Market Data & Events
        │
        ▼
Python Analytics Layer
(feature engineering, regimes, backtesting)
        │
        ▼
LLM Reasoning Layer
(event interpretation, scenario analysis)
        │
        ▼
Athsany Decision Engine
(direction bias, risk limits, strategy routing)
```

- **Market Data & Events**  
  - 價格與市場數據：FX、indices、gold、futures、oil、equities、derivatives  
  - 事件流：事件、政策、公佈數據等，統一時間軸管理並打上事件類型標籤  

- **Python Analytics Layer**  
  - 特徵工程：波動率、spread、結構性價位、跨資產相關性與 regime 判斷  
  - 回測與統計：不同事件類型在不同 regime 下，對各資產嘅歷史影響、hit‑rate 同 P&L 分佈  
  - 產出數值信號與風險指標，但唔直接下單  

- **LLM Reasoning Layer**  
  - 用大型語言模型，將非結構化文本（事件描述）轉成結構化「世界觀」  
  - 生成情景推演、風險敘述與解釋型文字，輔助人類理解決策背景  

- **Athsany Decision Engine**  
  - 綜合數據分析層與推理層輸入，輸出：  
    - Directional bias：多 / 空 / 中性  
    - Risk limits：倉位上限、槓桿限制、風險等級  
    - Strategy routing：可以啟用嘅策略類型及其風控參數  
  - 明確定位係 **decision support & risk management**，唔係「保證單一正確預測」

詳細架構拆解請見：[`docs/architecture.md`](docs/architecture.md)

---

## 7. Use cases / 應用場景

目前 demo 主要用 HSI 同 XAUUSD 作為示例，用嚟展示：

- 事件驅動視角 vs. 傳統裸 K 線 / 純粹技術分析  
- 喺大型事件（例如中東衝突、美伊事件）下，點樣：
  - 由「有事件」變成「世界雷達」  
  - 睇清楚邊啲板塊受實質衝擊、資金可能流向邊度  
  - 區分真正被拉動嘅資產 vs. 短期噪音

框架本身可以擴展到：

- 多資產組合風控  
- 保險 / AML / 房地產風險智能  
- 供應鏈、能源、零售、企業營運與政策情景推演等場景

更多示例請見：[`docs/use-cases.md`](docs/use-cases.md)

> 所有公開 use cases 均為 **概念示例 / prototype scenarios**，不構成任何投資建議或保證。

---

## 8. Prediction confidence / 預測信心層級（設計概念）

為避免「語氣過硬但實際機率有限」，Athsany 的決策設計中引入 **信心層級** 概念，用嚟標記每個輸出嘅可靠度：

- **High confidence（高信心）**  
  - 類似事件喺相同 regime 下歷史命中率高、樣本充足  
  - 可以給較明確方向同較積極倉位建議

- **Medium confidence（中信心）**  
  - 訊號方向一致但命中率中等，或者市場已部分 price‑in  
  - 偏向式建議（偏多／偏空、適度調整倉位）

- **Low confidence（低信心）**  
  - 訊號矛盾、樣本不足，或者 regime 正在轉換  
  - 只給風險提示同倉位上限建議，避免強行給方向

喺未來正式 UI / API 入面，每個決策輸出都會附帶 **信心標籤 + 風險級別**，方便一眼理解「呢個建議有幾硬、應該押幾重」。

---

## 9. Why Finance First, But Not Finance Only

Financial markets (e.g. HSI futures, XAUUSD) are our most complete demonstration environment today, not the final scope of Athsany.

Finance is an ideal sandbox because it provides:

- Dense, high‑frequency event streams  
- Clear outcomes and feedback loops  
- Well‑defined notions of risk, position, and performance

However, the core design of Athsany’s decision brain layer is **domain‑agnostic**.  
The same event → risk → strategy → execution → review pattern can be applied to:

- Enterprise and operational risk management  
- Supply chain and logistics decisions  
- Security / incident response  
- Any domain where events, risk, and long‑term decision evolution matter

**中文說明**

目前我們以 HSI、XAUUSD 等金融市場作為完整示範場景，因為金融可以提供高頻事件與清晰結果，方便驗證整個決策閉環。  
但 Athsany 的決策大腦層，從設計上就是面向任何需要事件理解、風險判斷與長期決策演化的領域，而不是只服務金融市場。

---

## 10. Roadmap / Status & Future

_Current status (will be updated as the system evolves):_

- ✅ Internal prototypes for event ingestion, decision logging, and memory structures  
- ✅ Demo use‑cases on HSI futures and XAUUSD to validate the full loop  
- 🚧 Building a more generalizable decision memory layer for non‑financial domains  
- 🚧 Preparing public demos and documentation  
- 🔭 Future: external API / SDK for integrating Athsany as a decision brain layer into other systems

---

## 11. Repository Structure (current & planned)

This repository is focused on **concepts and architecture**, not full production code (yet).

```text
.
├── docs/
│   ├── architecture.md        # High-level system architecture
│   ├── decision-loop.md       # Scenario → Event Cascade → Decision Output → Decision Memory
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

- Public specifications of Athsany’s decision brain architecture  
- Reference implementations and demo notebooks  
- Domain‑specific examples beyond finance

---

## 12. Disclaimer / 免責聲明

This repository focuses on **architecture, concepts, and non‑sensitive components** of the Athsany system.

- Production trading logic, proprietary strategy code and any confidential data sources are **not** included in this public repo.  
- The demo is an **early prototype** with **static scenarios and synthetic / simplified signals**, with **no live trading connectivity**.  
- Nothing in this repo or demo constitutes financial advice or a guarantee of performance.
