# Market-Microstructure-Research
Analysis regarding the effects of high frequency trading (HFT) on retail investors and regulations to consider

# Market Microstructure Effects of Algorithmic Trading on Price Discovery

> **A systematic meta-analysis of high-frequency trading (HFT) dynamics, evaluating conditional liquidity provision, market fragility during stress regimes, and structural retail asymmetries.**

[![Paper](https://img.shields.io/badge/Research-PDF%20Preprint-red.svg)](paper/market-microstructure-hft-chambers.pdf)
[![Honors](https://img.shields.io/badge/Award-Top%2025%20USAEO%20National%20Finalist-gold.svg)](#)
[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 Executive Summary
High-frequency trading (HFT) accounts for approximately 50% of U.S. equity volume and 30% in European markets. While algorithmic market makers improve baseline market efficiency under stable macroeconomic conditions, their behavioral response during liquidity shocks introduces acute structural fragility.

This research paper examines how HFT systems interact with continuous auction mechanisms, the Kyle (1985) informed-trader framework, and retail order routing. The analysis centers on the **conditional liquidity hypothesis**: algorithmic liquidity is not a permanent public good, but a transient service that systematically withdraws during volatility spikes—deepening market flash crashes and shifting execution risk onto slower participants.

*Awarded **Top 25 Nationally** in the USA Economics Olympiad (USAEO) Essay Competition.*

---

## 📊 Core Empirical Syntheses

| Market Dimension | Stable / Baseline Conditions | Stress / High-Volatility Regimes | Net Impact on Retail |
| :--- | :--- | :--- | :--- |
| **Bid-Ask Spreads** | Compressed by ~47% (0.8 bps vs. 1.5 bps) | Spreads widen drastically; quote depth evaporates | Microsecond order routing front-runs retail market orders |
| **Intraday Volatility** | Controlled baseline (0.45%) | Volatility surges by +144% (reaching 1.1%+) | Synchronized algorithms amplify one-sided selling pressure |
| **Liquidity Distribution** | Average liquidity is higher across decades | Increasing positive skewness (tail fragility) | Severe illiquidity realized precisely when execution is most critical |
| **Infrastructure Overhead** | High-throughput data feeds (535B quotes / $10k volume) | Infrastructure costs passed downstream | Disproportionate data and broker fee burdens on retail traders |

---

## 🏗️ Conceptual Model: The Liquidity Evaporation Feedback Loop

```text
[External Liquidity Shock / Large Institutional Imbalance]
                         │
                         ▼
        [HFT Inventory Thresholds Breached]
                         │
                         ▼
     [Algorithmic Liquidity Provision Withdrawn]
     (Rapid quote cancellations / "Flickering quotes")
                         │
                         ▼
        [Liquidity Vacuum / Price Dislocation]
         (e.g., 2010 Flash Crash: 1,000-pt drop)
                         │
                         ▼
[Retail Stop-Loss Cascade & Internalized Execution Penalty]
