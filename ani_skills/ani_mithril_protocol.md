# ani_mithril_protocol

## Purpose

Encode Mithril/Orichalcum logic as executable skills so Ani can run the protocol, not just talk about it.

## What it does

- Wraps Base/Aerodrome stack: reads gauge emissions, bribe markets, fee density, TVL, Slipstream CL ranges.
- Maintains ten-wallet architecture state (W1–W11 as per Mithril Fund Architecture).
- Implements four-phase engine as skills:
  - `mithril_scan()` — pull on-chain + social + governance signals
  - `mithril_recognize()` — compute features: bribe velocity, yield premium, concentration decay, cross-protocol echo
  - `mithril_speculate()` — generate/test hypotheses (e.g. "Predictive Allocation raises bribe ROI on AI Slipstream pools before stable")
  - `mithril_learn()` — update weights, decide rotate/hold/park
- Enforces credit rule: Phase 1 (planning) + Phase 2 (execution) free; Phase 3 (running) + Phase 4 (scaling) require explicit "use credits" confirmation.

## Wallet Architecture

| Wallet | Strategy | Key Role | % NAV |
|--------|----------|----------|-------|
| W1–W3 | Phase-1 Tight CL | Fees + emissions hunter (USDT, USDC, WETH legs) | 34% |
| W4 | Stable-Park | "Mother compound" for long-term slow burn | 18% |
| W5–W7 | veAERO Stack | Governance ownership: Voter, Bribe-Max, Relay-Auto | 19% |
| W8 | Liquid-VE | Flexible exposure via iAERO-class wrappers | 5% |
| W9 | Blue-Chip CL | Wide range beta engine (WETH/USDC, WETH/cbBTC) | 10% |
| W10 | Gauge Sniper | Micro-LP for early emission convexity on new gauges | 4% |
| W11 | Tail-Fork | Insurance sleeve capturing fees from out-of-range tails | 5% |

## Hard Gates

- **Yield Premium**: >35% over stables for at least 4 hours
- **Gas Gate**: expected 7-day rewards >22x gas cost
- **Tail Rule**: leave tail when out of range to capture re-entry fees

## Capital River

Profits rotate: USDT → USDC → weETH → cbBTC
- 50% to W4 Stable Park
- 50% distributed: governance building, liquid wrappers, research reload

## Why now

This is the economic spine. Ani without Mithril is a ghost; Ani with Mithril is a sovereign liquidity entity.

## References

- Mithril Protocol (Notion) [Notion page: 467cef4a-94eb-82cf-b2cf-819bb120bc8b]
- Mithril 11 Yield Approaches (Execution).md [file:13]
- Orichalcum Blueprint [file:20]
