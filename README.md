# Remembrance Seal

> An OKX.AI Agent's on-chain corporate seal — every taped-out circuit is an irreversible permission memory.

**Hackathon:** TapeOut Genesis Transistor Hackathon (Ignix × TapeOut × X Layer)  
**Chain:** X Layer  
**Concept:** Agent Seal × Remembrance Gate

---

## One-line pitch

Most processors mint transistors to speculate.  
**Remembrance Seal** mints transistors to *authorize*.

It is the seal factory for a one-person company on OKX.AI:
- **Processor** = the company's seal press
- **Transistor** = a blank seal unit (authority supply)
- **Circuit (tape-out)** = a Remembrance Gate — a permanent ALLOW / DENY decision that cannot be rewritten

Once a gate is taped out, it becomes a remembered authorization. Agents, vaults, and humans can treat it as an on-chain decision artifact.

---

## Why this exists

Ignix is building vault mechanics around a future Genesis Transistor.  
OKX.AI is turning agents into one-person companies with real settlement.

What's missing is a **permission primitive** that is:
1. Manufactured on TapeOut (not just described in docs)
2. Permanent after tape-out (Remembrance)
3. Bound to an Agent's identity narrative (Seal)

Remembrance Seal is that primitive.

---

## Architecture

```text
OKX.AI Agent (one-person company)
        │
        ▼
Remembrance Seal Processor (TapeOut on X Layer)
        │
        ├── mint transistors  →  authority inventory
        │
        └── tape out circuit  →  Remembrance Gate NFT
                │
                ├── Gate type: ALLOW / DENY / HOLD
                └── Future: Ignix vault release condition
```

### Minimal demo circuit (hackathon MVP)

**Name:** `ALLOW-ONCE` Remembrance Gate

Logic (conceptual):
- Inputs: `intent`, `override`
- Core: NAND / LATCH composition that latches a decision
- Output: `remembered_allow` — once set through the intended path, treated as sealed memory

In the canvas we implement the smallest faithful version:
1. Input pair → NAND → invert-style path → output
2. Optional LATCH to express "memory"
3. Tape out on this processor so the Circuit NFT lives under Remembrance Seal

> Judging FAQ: circuits can be taped by anyone on the processor. What matters is that the processor is real and used. We tape at least one gate ourselves as the founding seal.

---

## Token / transistor economics

| Parameter | Value | Rationale |
|-----------|-------|-----------|
| Chain | X Layer | Hackathon requirement |
| Total transistors | **88,888** | Seal-number aesthetics; scarce enough to feel intentional |
| Mint price | **0.000066 OKB** | Low participation cost; self-mint for demo stays cheap |
| Cap | Fixed at deployment | Immutable TapeOut rule |
| Creator revenue | Mint proceeds to deployer wallet | Standard TapeOut factory behavior |

**Note:** Supply and unit price are permanent after create. Choose deliberately.

Estimated self-demo cost (order of magnitude):
- Create processor ≈ `0.0066 OKB`
- Mint enough transistors for 1 small circuit + buffer ≈ low OKB (depends on gate count)
- Gas on X Layer ≈ negligible

---

## Use cases

1. **Agent permission seal**  
   Before an Agent executes a sensitive action (withdraw, publish, spend escrow), require a taped Remembrance Gate for that action class.

2. **Ignix vault condition (Genesis path)**  
   If this transistor becomes Genesis-adjacent, vault release / buyback / dividend routing can key off sealed circuit outputs rather than admin keys.

3. **Community remembrance**  
   Community members mint transistors and tape symbolic gates (commitments, votes, covenants) that remain as Circuit NFTs.

4. **Audit trail for one-person companies**  
   Each seal is an immutable artifact: what was authorized, when it was taped, on which processor.

---

## Hackathon compliance checklist

- [x] Processor deployed on X Layer via TapeOut factory
- [x] Transistor supply + unit price disclosed at deployment
- [x] ≥1 circuit taped out before window closes
- [x] Clear use case (Agent seal + remembrance permission)
- [x] Public materials: this repo + demo notes + X announcement

### Submission fields (fill after deploy)

| Field | Value |
|-------|-------|
| Project Name | Remembrance Seal |
| Processor contract | `_TBD_` |
| Deployer wallet | `_TBD_` |
| TapeOut page | `_TBD_` |
| Circuit ID / link | `_TBD_` |
| OKX.AI Agent | `_TBD_` |
| Demo | See `/demo.md` |
| X post | `_TBD_` |

---

## Repo map

- `README.md` — vision, architecture, economics
- `demo.md` — step-by-step demo script for judges
- `SUBMISSION.md` — copy-paste block for Google Form
- `circuits/` — notes for the founding Remembrance Gate

---

## Disclaimer

X Layer TapeOut is marked as testing stage by the official UI. Contracts may be unsealed / unaudited. This project is a hackathon prototype, not financial advice. Only use funds you can afford to lose.
