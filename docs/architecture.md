# Athsany Architecture – Decision Brain Layer

Athsany is an always‑on **Decision Brain / Decision Memory System** that lives above information and data sources, not a chat‑first tool.

## Design Goals

- Run as an always‑on decision brain above information streams and data sources  
- Focus on high‑uncertainty, information‑ and event‑driven decisions  
- Build long‑term decision memory and self‑correction, not just one‑off signals  

**中文說明**  
Athsany 的架構目標不是做一個聊天界面，而是建立一個常駐在資訊與數據上層的「決策大腦層」。  
它專注處理高不確定、由資訊／事件驅動的決策，同時為每一次決策建立可回溯的長期記憶與自我修正能力。

## High‑Level Components

> 下列是概念層的元件，著重職責，而不涉及具體實作細節。

- **Information ingestion layer** – 連接資訊、數據源、市場行情或其他外部／內部資訊來源，統一時間軸與基本結構  
- **Risk & context modeling** – 把資訊轉換為可用來決策的風險狀態與情境視圖（exposure、timing、scenarios 等）  
- **Strategy & action engine** – 基於當前風險視圖與歷史 decision memory，產生或調整策略及建議行動  
- **Execution interface** – 把策略／建議轉成實際動作（下單、資源調配、提示、風控規則等），與外部系統整合  
- **Decision memory store** – 記錄決策、行動、結果、偏差與事後反思，供之後查詢與學習  
- **Explanation / review module** – 協助解釋「為什麼這樣決策、錯在哪、下次應該如何調整」，支援審核與檢討

## Layers Overview

從更抽象的角度，Athsany 可以被視為三層疊加的結構：

- **Interface layer** – where humans and other systems see Athsany (dashboards, APIs, alerts)  
- **Decision brain layer** – the core loop and decision memory (this repo focuses on this layer)  
- **Execution / integration layer** – connectors to trading systems, risk engines, or other operational systems  

（詳細的內部細分，例如資訊輸入、風險視圖、行動映射、風險護欄、執行控制台與決策記憶，可在架構圖中看到，但不在文字中逐一展開。）

## Documentation Status

This document currently focuses on the core **decision brain layer**.

Planned additions:

- More detail on how decision memory is persisted and queried  
- Examples of information / event and risk schemas across different domains  
- Integration patterns with existing trading, risk, and operational systems
