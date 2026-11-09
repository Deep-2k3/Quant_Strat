# Quant_Strat — Futures Trading Strategies, ICT/SMC Indicators & Risk Tools

**[Quant\_Strat](https://www.google.com/search?q=https://github.com/Deep-2k3/Quant_Strat)** is a quantitative trading repository containing custom automated strategies, Smart Money Concepts (SMC) / ICT market-structure indicators, and chart-integrated risk management utilities for futures trading (including **NQ / MNQ**, **ES / MES**, and **GC / MGC**). Built in **C# ([NinjaScript](https://docs.ninjatrader.com/ninjascript_explorer) / WPF)** for NinjaTrader 8 and **[Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)** for TradingView.

## Repository Contents

### 1. Strategies (Automated & Systematic Execution)

| File Name | Platform & Language | Description |
| :--- | :--- | :--- |
| **`PivotPointSTRAT.zip`** | [NinjaTrader 8 (C#)](https://docs.ninjatrader.com/ninjascript_explorer) | Automated NinjaScript strategy package built around structural pivot points and multi-session inflection levels. |
| **`SMC Expo Strat (TV)`** | [TradingView (Pine Script)](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/) | Smart Money Concepts (SMC) execution strategy script tailored for Micro Gold (`MGC`) and index futures. |
| **`SMC Expo V2`** | [TradingView (Pine Script)](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/) | **SMC Precision Flow v2** — upgraded TradingView strategy featuring refined order-flow and market-structure entry filters. |

### 2. Market-Structure & Liquidity Indicators (ICT / FVG / Levels)

| File Name | Platform & Language | Description |
| :--- | :--- | :--- |
| **`FOProFVGEQ`** | [NinjaTrader 8 (C#)](https://docs.ninjatrader.com/ninjascript_explorer) | Plots Fair Value Gaps (FVGs), Inversion FVGs (iFVGs), session killzones, key time-based liquidity levels, and range equilibrium (`EQ`) lines on NinjaTrader 8 charts. |
| **`Pro FVG + ICT Killzones (TV)`** | [TradingView (Pine Script)](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/) | TradingView counterpart to `FOProFVGEQ`; plots ICT session killzones, FVGs/iFVGs, time-based liquidity levels, and equilibrium (`EQ`) lines. |
| **`RIPS Levels`** | [TradingView (Pine Script)](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/) | Plots structured RIPS weekly reference and liquidity levels on TradingView charts. |
| **`Rips levels (NT8)`** | [NinjaTrader 8 (C#)](https://docs.ninjatrader.com/ninjascript_explorer) | NinjaTrader 8 implementation of the `RipsLevels` indicator integrated with an on-chart Average True Range (ATR) table. |

### 3. On-Chart Risk & Execution Utilities (WPF / NinjaScript)

| File Name | Platform & Language | Description |
| :--- | :--- | :--- |
| **`RRtool.txt`** | [NinjaTrader 8 (C#)](https://docs.ninjatrader.com/ninjascript_explorer) | Updated Risk-to-Reward (`R:R`) and dynamic position-sizing utility designed for fast manual futures execution and prop-firm drawdown management. |
| **`Risk Assistant`** | [NinjaTrader 8 (C# / WPF)](https://docs.ninjatrader.com/ninjascript_explorer) | On-chart risk management indicator featuring custom Windows Presentation Foundation (WPF) UI controls (earlier architecture of `RRtool`). |

## Installation & Setup

### NinjaTrader 8 Scripts & Archives
1. **For `.zip` Strategy Archives (`PivotPointSTRAT.zip`):** In NinjaTrader 8, open the Control Center and go to **Tools > Import > NinjaScript Add-On...**, select the `.zip` archive, and import ([NinjaTrader Distribution Procedure](https://ninjatrader.com/support/helpguides/nt8/distribution_procedure.htm)).
2. **For Individual C# Scripts (`FOProFVGEQ`, `Rips levels (NT8)`, `Risk Assistant`, `RRtool.txt`):** Copy the code into a `.cs` file inside `Documents\NinjaTrader 8\bin\Custom\Indicators\` (or `Strategies\`), open **New > NinjaScript Editor**, and press **F5** to compile ([NinjaScript Explorer Docs](https://docs.ninjatrader.com/ninjascript_explorer)).

### TradingView Scripts
1. Open a chart on TradingView and click **Pine Editor** in the bottom panel ([TradingView Pine Editor Guide](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)).
2. Copy the script from **`Pro FVG + ICT Killzones (TV)`**, **`RIPS Levels`**, **`SMC Expo Strat (TV)`**, or **`SMC Expo V2`**, paste it into the editor, click **Save**, and select **Add to chart**.

## Ongoing Development Focus

* **Cross-Platform Feature Parity:** Synchronizing ICT FVG/iFVG, equilibrium, and RIPS level logic between TradingView Pine Script and NinjaTrader 8 C#.
* **WPF Chart Trader Ergonomics:** Expanding `RRtool` and `Risk Assistant` with automated contract calculations, one-click breakeven triggers, and daily loss limit locks.
* **Macro Volatility Filters:** Adding pre-release session locks around high-impact ("red folder") US economic calendar events.

## Disclaimer

All strategies, indicators, and utilities in this repository are provided strictly for quantitative research, backtesting, and educational purposes. Futures trading involves substantial risk of loss.