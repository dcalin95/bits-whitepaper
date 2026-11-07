---
icon: battle-net
---

# BITS Neural Intelligence

## BITS Neural Intelligence – AI Trading & Liquidity Engine

### 1. Vision

BITS Neural Intelligence is the AI core of BitSwapDEX\_AI, designed to go beyond traditional liquidity tools such as Kima's LIMA. While LIMA focuses on liquidity research and insights, BITS Neural Intelligence provides a full-stack AI layer for **research, decision-making, risk management and execution** across the BitSwapDEX ecosystem.

Our goal is to give users institutional-grade trading and liquidity intelligence, while maintaining strict risk controls and a clear regulatory alignment.

***

### 2. Core Design Principles

* **User-first & non-custodial**: Users keep control of their keys wherever possible. AI acts as a tool, not as an uncontrolled black box.
* **Progressive automation**: Three modes – Research, Co-Pilot, Auto-Pilot – with clear separation and explicit user consent.
* **Risk-aware by design**: Risk limits, exposure controls, and market-abuse prevention are built in from day one.
* **Transparent AI**: Every AI decision (signal, trade, parameter change) is logged and explainable at the user and governance level.
* **Regulatory-aware**: Architecture is compatible with future licensing (MiCA CASP / VASP-style regimes) and jurisdictional constraints.

***

### 3. Capabilities

#### 3.1 Research Mode

* Real-time monitoring of BitSwapDEX order books, trades and liquidity.
* On-chain data and external market data aggregation (where available).
* Detection of:
  * liquidity gaps,
  * spread anomalies,
  * volume spikes and volatility regimes.
* Outputs:
  * dashboards,
  * alerts,
  * quantitative scores (liquidity score, volatility score, trend score).

#### 3.2 Co-Pilot Mode

* AI proposes concrete trades, but the **user confirms** each execution:
  * "Buy 1,250 BITS with USDT at limit price X"
  * "Rebalance 20% from BITS/USDT to BITS/BNB"
* Strategy library:
  * market making on BITS pairs,
  * trend-following,
  * mean-reversion,
  * smart DCA for accumulators.
* Each signal is accompanied by:
  * rationale (trend, volatility, liquidity),
  * risk level (Low/Medium/High),
  * impact on the user's portfolio.

#### 3.3 Auto-Pilot Mode (future, licensed)

> **Note:** This mode will only be available subject to regulatory approvals and local licensing requirements.

* The AI is allowed to execute trades automatically within predefined risk limits:
  * max position size per pair,
  * global drawdown limit,
  * leverage restrictions (if applicable).
* Execution engine continuously:
  * updates quotes,
  * manages open orders,
  * reacts to market conditions,
  * enforces risk rules and circuit breakers.

***

### 4. System Architecture

#### 4.1 High-Level Components

* **Neural Intelligence UI (bits-ai.io)**
  * "Neural Intelligence" dashboard.
  * User configuration (risk preferences, pairs, modes).
  * Trade signal history and AI decisions log.
* **API Gateway**
  * REST/JSON endpoints for UI and external services.
  * Authentication, rate-limiting, and auditing.
* **BITS AI Orchestrator**
  * Central AI service coordinating models, strategies and risk.
  * Pulls data from the Market Data Service and Order/Position Service.
* **Market Data Service**
  * Streams order books, trades and OHLC from the BitSwapDEX matching engine.
  * Optionally ingests external reference prices.
* **Strategy Engine**
  * Library of strategies (market making, trend, mean-reversion, DCA).
  * Each strategy is parameterized, backtestable and versioned.
* **Risk & Compliance Engine**
  * Pre-trade and post-trade checks.
  * User-level limits, exposure controls and anomaly detection.
  * Market abuse and manipulation prevention logic.
* **Execution Engine**
  * Connects to the BitSwapDEX matching engine.
  * Places, modifies and cancels orders.
  * Guarantees safety (no runaway order loops, no invalid orders).
* **Data Lake & Audit Log**
  * Stores:
    * user configs,
    * AI signals,
    * executed trades,
    * model versions and parameters.
  * Enables full audit trail and governance oversight.

***

### 5. Interaction with the BITS Token

* BITS can be used as:
  * a core asset for AI-driven strategies,
  * a staking mechanism to access advanced AI features,
  * a potential reward layer for providing liquidity that is actively managed by the AI.
* Governance may decide:
  * which strategies are enabled by default,
  * what risk limits apply to AI-managed liquidity pools,
  * how fees from AI-managed strategies are shared with BITS stakers.

(Details of tokenomics are specified in the main BITS token section.)

***

### 6. Security & Transparency

* **Key security**:
  * Whenever possible, AI operates with limited-scoped API keys or smart contracts with constrained permissions.
* **Model transparency**:
  * Versioned models, with changelog and governance visibility.
  * Clear indication when models are retrained or upgraded.
* **Fail-safe design**:
  * Circuit breakers to stop trading under abnormal conditions.
  * Manual override by operations / governance.

***

### 7. Regulatory & Compliance Approach

* BITS Neural Intelligence is designed under the assumption that:
  * Any mode where the AI **executes trades for users** may qualify as algorithmic trading / portfolio management under EU financial services rules.
  * Crypto-asset services like operating a trading platform or executing orders for clients fall under the MiCA CASP regime in the EU.
* Therefore:
  * Research and Co-Pilot modes are prioritized at launch.
  * Auto-Pilot modes will only be activated where and when the necessary licenses and registrations (e.g., CASP / VASP / investment firm) are in place.
  * Geofencing and KYC/AML controls are enforced to comply with local regulations.

Users are clearly informed that AI tools are experimental, involve risk, and do not guarantee profits.

***

### 8. Roadmap

1. **Phase 1 – Research Mode**
   * Liquidity dashboards and AI analytics for BITS and core pairs.
   * Telegram/Discord bot integration for alerts.
2. **Phase 2 – Co-Pilot Mode**
   * Signal generation and one-click trade confirmation from the UI.
   * Basic strategy templates (market making, DCA, trend).
3. **Phase 3 – Auto-Pilot (Licensed)**
   * Full AI-assisted execution for selected jurisdictions and user segments.
   * Advanced strategies, portfolio-level optimization, and cross-market routing.
4. **Phase 4 – Governance Integration**
   * Community voting on model upgrades, risk parameters and strategy mix.
